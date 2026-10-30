# Hardened elasticsearch_exporter image

Built and scanned on 2026-10-19 with Docker Scout v1.15.0.

Image: `elasticsearch_exporter:critical-fixed` (linux/amd64).
Image ID: `sha256:86280f276328a8b93dbbf67cc51c6b0c870505867e5f01828a1eb4a2d8748832`.
Source revision: `d8e014046d78275052540b952696d91b3edf246e`.
Version: `1.11.0-dev.d8e0140`. This is a build of the checked-out development
source, not the published v1.11.0 release.

## Scan results

| Severity | Original local upstream image | Hardened image |
| --- | ---: | ---: |
| Critical | 7 | 0 |
| High | 37 | 0 |
| Medium | 8 | 0 |
| Low | 0 | 0 |
| Unspecified | 2 | 1 |

Original image: `quay.io/prometheuscommunity/elasticsearch-exporter:latest`,
ID `sha256:b217bc774a0601d1a2ae93a64db9d6e11cdea6afb5ceae62aaaa3ee51eadd3d1`.
Counts are Scout findings, including the same advisory against multiple package
identities; they are not counts of unique CVE IDs.

Full unfiltered reports are in `security-reports/before.md` and
`security-reports/after.md`; machine-readable output is in
`security-reports/after.sarif.json`. No suppressions or VEX overrides were added.

The remaining unspecified advisory is GO-2026-5932 against
`golang.org/x/crypto v0.58.0`, concerning the unmaintained `openpgp` package.
Scout reports no fixed version. This module-level finding is retained in the
report. The image is not claimed to have zero findings of every severity.
Scan results reflect the vulnerability database at the time of the scan.

## Build

Run from this repository root in PowerShell:

```powershell
$exporterRevision = git rev-parse HEAD
docker build --pull --platform linux/amd64 -f Dockerfile.hardened --build-arg "REVISION=$exporterRevision" --build-arg VERSION=1.11.0-dev.d8e0140 -t elasticsearch_exporter:critical-fixed .
docker scout cves --exit-code --only-severity critical,high local://elasticsearch_exporter:critical-fixed
```

The separate Dockerfile uses Go 1.27.2 pinned by image digest, verifies module
checksums, runs all existing Go tests, and builds with CGO disabled. It uses the
existing checked-in go.mod and go.sum, whose dependencies are already newer
than those in the original image. The final scratch image includes the static
exporter binary, CA certificates, nobody user/group files, /tmp, and LICENSE.
It runs as UID/GID 65534. No shell or package manager is included.

## Load and run

The exported archive and SHA256 checksum are one directory above this repository:

```powershell
docker load --input ..\elasticsearch_exporter-critical-fixed-linux-amd64.tar
docker run --rm -p 7979:7979 elasticsearch_exporter:critical-fixed --web.listen-address=:7979 --es.uri=http://YOUR_ELASTICSEARCH_OR_OPENSEARCH:9200
```

Replace the backend address with one reachable from the container. Explicitly
pass `--es.uri` for single-target collection: this development source defaults
to multi-target mode. The metrics endpoint is `/metrics`; health is `/healthz`.
Custom CA/client certificates and exporter configuration can be mounted read-only.

## Validation

- `go mod verify`: passed during the image build.
- `go test -count=1 ./...`: all packages with tests passed during the build.
- `--version`: confirms Go 1.27.2 and the source revision above.
- Runtime smoke test: `/healthz` HTTP 200, `/metrics` HTTP 200 with exporter build
  info and Go 1.27.2, and `/probe` without target HTTP 400.
- Smoke test ran non-root, with a read-only root filesystem, tmpfs /tmp,
  all capabilities dropped and no-new-privileges. See `security-reports/smoke-test.txt`.
- Scout Critical/High gate: passed (exit code 0).

No live Elasticsearch/OpenSearch cluster was available for an end-to-end scrape;
the existing collector tests exercised fixture-backed HTTP servers.
