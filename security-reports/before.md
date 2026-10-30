<h2>:mag: Vulnerabilities of <code>quay.io/prometheuscommunity/elasticsearch-exporter:latest</code></h2>

<details open="true"><summary>:package: Image Reference</strong> <code>quay.io/prometheuscommunity/elasticsearch-exporter:latest</code></summary>
<table>
<tr><td>digest</td><td><code>sha256:b217bc774a0601d1a2ae93a64db9d6e11cdea6afb5ceae62aaaa3ee51eadd3d1</code></td><tr><tr><td>vulnerabilities</td><td><img alt="critical: 7" src="https://img.shields.io/badge/critical-7-8b1924"/> <img alt="high: 37" src="https://img.shields.io/badge/high-37-e25d68"/> <img alt="medium: 8" src="https://img.shields.io/badge/medium-8-fbb552"/> <img alt="low: 0" src="https://img.shields.io/badge/low-0-lightgrey"/> <img alt="unspecified: 2" src="https://img.shields.io/badge/unspecified-2-lightgrey"/></td></tr>
<tr><td>size</td><td>10 MB</td></tr>
<tr><td>packages</td><td>48</td></tr>
</table>
</details></table>
</details>

<table>
<tr><td valign="top">
<details><summary><img alt="critical: 3" src="https://img.shields.io/badge/C-3-8b1924"/> <img alt="high: 14" src="https://img.shields.io/badge/H-14-e25d68"/> <img alt="medium: 4" src="https://img.shields.io/badge/M-4-fbb552"/> <img alt="low: 0" src="https://img.shields.io/badge/L-0-lightgrey"/> <!-- unspecified: 0 --><strong>stdlib</strong> <code>go1.26.5</code> (golang)</summary>

<small><code>pkg:golang/stdlib@go1.26.5</code></small><br/>
<a href="https://scout.docker.com/v/CVE-2026-56857?s=golang&n=stdlib&t=golang&vr=%3C1.26.9"><img alt="critical : CVE--2026--56857" src="https://img.shields.io/badge/CVE--2026--56857-lightgrey?label=critical%20&labelColor=8b1924"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.26.9</code></td></tr>
<tr><td>Fixed version</td><td><code>1.26.9</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.49%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>41st percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

On Windows, when the target of Root.Mkdir or Root.MkdirAll is a junction pointing to an empty location, the operation can create a directory at the junction target even when that target is located outside the root. This only applies to operations where the last path component is a junction (path/to/junction, but not path/junction/target).

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-39821?s=golang&n=stdlib&t=golang&vr=%3E%3D1.26.0-0%2C%3C1.26.6"><img alt="critical : CVE--2026--39821" src="https://img.shields.io/badge/CVE--2026--39821-lightgrey?label=critical%20&labelColor=8b1924"/></a> 

<table>
<tr><td>Affected range</td><td><code>>=1.26.0-0<br/><1.26.6</code></td></tr>
<tr><td>Fixed version</td><td><code>1.26.6</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.69%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>52nd percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

The ToASCII and ToUnicode functions incorrectly accept Punycode-encoded labels that decode to an ASCII-only label. For example, ToUnicode("xn--example-.com") incorrectly returns the name "example.com" rather than an error.

This behavior can lead to privilege escalation in programs using the idna package. For example, a program which performs privilege checks on the ASCII hostname may reject "example.com" but permit "xn--example-.com". If that program subsequently converts the ASCII hostname to Unicode, it will inadvertently permits access to the Unicode name "example.com".

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-78663?s=golang&n=stdlib&t=golang&vr=%3C1.26.9"><img alt="critical : CVE--2026--78663" src="https://img.shields.io/badge/CVE--2026--78663-lightgrey?label=critical%20&labelColor=8b1924"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.26.9</code></td></tr>
<tr><td>Fixed version</td><td><code>1.26.9</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.57%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>46th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

The HTTP/2 server can refund connection-level flow control twice for the same data: Once when a client resets a stream (refunding data for any sent-but-unread portion of the stream), and again when a request handler reads the buffered data. A malicious client can exploit this to bypass the configured connection-level flow control limit (MaxReceiveBufferPerConnection). Total buffered data is still limited by the concurrent stream limit and stream-level flow control.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-97032?s=golang&n=stdlib&t=golang&vr=%3C1.26.9"><img alt="high : CVE--2026--97032" src="https://img.shields.io/badge/CVE--2026--97032-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.26.9</code></td></tr>
<tr><td>Fixed version</td><td><code>1.26.9</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.42%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>35th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

HTTP/2 servers could end up crashing due to inadvertently modifying its HPACK encoder concurrently. This happens because the server modifies the HPACK encoder from two goroutines without synchronization: one uses the encoder to encode a HEADERS frame as part of a response sent to a client and the other modifies the encoder's table size when handling a SETTINGS frame containing SETTINGS_HEADER_TABLE_SIZE that a client sends. A malicious client can repeatedly send a request while changing the header table size to crash the server.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-97031?s=golang&n=stdlib&t=golang&vr=%3C1.26.9"><img alt="high : CVE--2026--97031" src="https://img.shields.io/badge/CVE--2026--97031-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.26.9</code></td></tr>
<tr><td>Fixed version</td><td><code>1.26.9</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.39%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>32nd percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

Multiple ECH outer extension references are not permitted under RFC 9849; previously, a client could send a well-crafted packet that could trigger memory exhaustion in the server process by specifying multiple references.

We now reject these as malformed and curb the memory amplification vector as a result.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-94440?s=golang&n=stdlib&t=golang&vr=%3C1.26.9"><img alt="high : CVE--2026--94440" src="https://img.shields.io/badge/CVE--2026--94440-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.26.9</code></td></tr>
<tr><td>Fixed version</td><td><code>1.26.9</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.40%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>33rd percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

Parsing a multipart form can bypass memory limits and read an arbitrarily long line into memory when the remaining limit at the start of a part is less than 400 bytes.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-94439?s=golang&n=stdlib&t=golang&vr=%3C1.26.9"><img alt="high : CVE--2026--94439" src="https://img.shields.io/badge/CVE--2026--94439-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.26.9</code></td></tr>
<tr><td>Fixed version</td><td><code>1.26.9</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.31%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>23rd percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

When an HTTP server handler sends a 2xx response to an HTTP/1 CONNECT request and returns without hijacking the connection, the server improperly continues to read and serve requests from the connection. Since a 2xx response to an HTTP/1 CONNECT converts the connection into a tunnel, the server should not treat the connection as continuing to contain HTTP.

The impact of this misbehavior is mostly limited to potential request smuggling, where an intermediate proxy considers the data on the connection to be tunneled and the server considers it to be HTTP.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-78669?s=golang&n=stdlib&t=golang&vr=%3C1.26.9"><img alt="high : CVE--2026--78669" src="https://img.shields.io/badge/CVE--2026--78669-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.26.9</code></td></tr>
<tr><td>Fixed version</td><td><code>1.26.9</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.57%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>46th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

A malicious HTTP/2 peer can cause excessive CPU consumption in the client or server by opening a large number of streams and then sending many small SETTINGS frames containing SETTINGS_INITIAL_WINDOW_SIZE values.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-78667?s=golang&n=stdlib&t=golang&vr=%3C1.26.9"><img alt="high : CVE--2026--78667" src="https://img.shields.io/badge/CVE--2026--78667-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.26.9</code></td></tr>
<tr><td>Fixed version</td><td><code>1.26.9</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.38%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>30th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

When parsing a Range header containing a large number of small ranges, FileServer(FS), ServeContent, and ServeFile(FS) can consume an excessive amount of CPU.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-78660?s=golang&n=stdlib&t=golang&vr=%3C1.26.9"><img alt="high : CVE--2026--78660" src="https://img.shields.io/badge/CVE--2026--78660-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.26.9</code></td></tr>
<tr><td>Fixed version</td><td><code>1.26.9</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.30%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>22nd percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

Historically, we have been rather lax about malformed framing-related headers in our HTTP/2 implementation, as they cannot interfere with HTTP/2 framing. However, this makes it possible for our HTTP/2 implementation to forward responses containing such headers to an HTTP/1 client when acting as a reverse proxy. If the HTTP/1 client also does not behave strictly enough, this can result in response smuggling.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-78659?s=golang&n=stdlib&t=golang&vr=%3C1.26.9"><img alt="high : CVE--2026--78659" src="https://img.shields.io/badge/CVE--2026--78659-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.26.9</code></td></tr>
<tr><td>Fixed version</td><td><code>1.26.9</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.57%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>46th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

When "Trailer" headers are sent by a client, the HTTP server internally uses the header values to populate the Request.Trailer map passed to the server handler. Because Request.Trailer is a map, each entry incurs memory overhead. For HTTP/2 servers, a malicious client can exploit this by sending a "Trailer" header that declares a large number of fields, causing the server to allocate a disproportionate amount of memory while bypassing Server.MaxHeaderValueCount and Server.MaxHeaderBytes limits. This exploit is not applicable for HTTP/1 servers, which do not support multiplexing a large number of requests over one TCP connection, and whose Server.MaxHeaderBytes are calculated differently.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-56866?s=golang&n=stdlib&t=golang&vr=%3C1.26.9"><img alt="high : CVE--2026--56866" src="https://img.shields.io/badge/CVE--2026--56866-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.26.9</code></td></tr>
<tr><td>Fixed version</td><td><code>1.26.9</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.31%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>22nd percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

When http.Transport sends an HTTP/1 CONNECT request with a non-empty Request.Body, it writes the body directly to the connection without framing after the request headers. If the server rejects the CONNECT request with a non-2xx keep-alive response, Transport returns the connection to the idle pool. Because CONNECT requests do not have a request body, the server may interpret the trailing body bytes as a subsequent pipelined HTTP/1.1 request on the connection, leaving the pooled connection desynchronized and causing the next caller that reuses it to read the response to the injected request. In reverse proxies (including httputil.ReverseProxy) that forward CONNECT requests through a shared Transport, this can lead to cross-user response poisoning.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-56862?s=golang&n=stdlib&t=golang&vr=%3E%3D1.26.0-0%2C%3C1.26.6"><img alt="high : CVE--2026--56862" src="https://img.shields.io/badge/CVE--2026--56862-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code>>=1.26.0-0<br/><1.26.6</code></td></tr>
<tr><td>Fixed version</td><td><code>1.26.6</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.57%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>46th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

Handshake messages, such as KeyUpdate, are always considered as state-advancing, regardless of whether a handshake has been completed or not. As a result, a malicious client can keep sending KeyUpdate messages to force the server to keep performing key derivation operations indefinitely.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-56859?s=golang&n=stdlib&t=golang&vr=%3E%3D1.26.0-0%2C%3C1.26.6"><img alt="high : CVE--2026--56859" src="https://img.shields.io/badge/CVE--2026--56859-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code>>=1.26.0-0<br/><1.26.6</code></td></tr>
<tr><td>Fixed version</td><td><code>1.26.6</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.57%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>46th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

Previously, DecodeElement would reset the depth counter causing it to never fire; this could lead to stack exhaustion.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-56853?s=golang&n=stdlib&t=golang&vr=%3E%3D1.26.0-0%2C%3C1.26.6"><img alt="high : CVE--2026--56853" src="https://img.shields.io/badge/CVE--2026--56853-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code>>=1.26.0-0<br/><1.26.6</code></td></tr>
<tr><td>Fixed version</td><td><code>1.26.6</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.57%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>46th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

When a server is configured to support unencrypted HTTP/2, it reads a few bytes from each new connection to see if they contain the HTTP/2 client preface. ReadHeaderTimeout is unexpectedly not being applied when doing this.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-46600?s=golang&n=stdlib&t=golang&vr=%3E%3D1.26.0-0%2C%3C1.26.6"><img alt="high : CVE--2026--46600" src="https://img.shields.io/badge/CVE--2026--46600-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code>>=1.26.0-0<br/><1.26.6</code></td></tr>
<tr><td>Fixed version</td><td><code>1.26.6</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.55%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>45th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

Parsing an invalid SVCB or HTTPS RR can panic when the size of a parameter value overflows the message buffer.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-33818?s=golang&n=stdlib&t=golang&vr=%3E%3D1.26.0-0%2C%3C1.26.6"><img alt="high : CVE--2026--33818" src="https://img.shields.io/badge/CVE--2026--33818-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code>>=1.26.0-0<br/><1.26.6</code></td></tr>
<tr><td>Fixed version</td><td><code>1.26.6</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.57%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>46th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

Enforce a recursion limit in Unmarshal to prevent stack exhaustion when parsing deeply-nested, recursive structures.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-97030?s=golang&n=stdlib&t=golang&vr=%3C1.26.9"><img alt="medium : CVE--2026--97030" src="https://img.shields.io/badge/CVE--2026--97030-lightgrey?label=medium%20&labelColor=fbb552"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.26.9</code></td></tr>
<tr><td>Fixed version</td><td><code>1.26.9</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.20%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>9th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

A trusted template author may have previously written a valid template wherein the use of the 'yield' keyword would not be correctly escaped.

We now ensure that valid keyword uses are escaped and non-keyword uses are not escaped.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-94448?s=golang&n=stdlib&t=golang&vr=%3C1.26.9"><img alt="medium : CVE--2026--94448" src="https://img.shields.io/badge/CVE--2026--94448-lightgrey?label=medium%20&labelColor=fbb552"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.26.9</code></td></tr>
<tr><td>Fixed version</td><td><code>1.26.9</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.20%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>9th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

When a JavaScript template literal contains consecutive expressions, the context tracking state was not properly reset upon entering a new expression.

We now ensure that template-literal expression entries correctly reset context variables so all subsequent regular expression literals are accurately recognized and escaped.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-56858?s=golang&n=stdlib&t=golang&vr=%3E%3D1.26.0-0%2C%3C1.26.6"><img alt="medium : CVE--2026--56858" src="https://img.shields.io/badge/CVE--2026--56858-lightgrey?label=medium%20&labelColor=fbb552"/></a> 

<table>
<tr><td>Affected range</td><td><code>>=1.26.0-0<br/><1.26.6</code></td></tr>
<tr><td>Fixed version</td><td><code>1.26.6</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.31%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>22nd percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

Previously, pathological inputs could close an unescaped '/' early, allowing for attack-controlled data to inject arbitrary content, potentially leading to XSS.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-56860?s=golang&n=stdlib&t=golang&vr=%3E%3D1.26.0-0%2C%3C1.26.6"><img alt="medium : CVE--2026--56860" src="https://img.shields.io/badge/CVE--2026--56860-lightgrey?label=medium%20&labelColor=fbb552"/></a> 

<table>
<tr><td>Affected range</td><td><code>>=1.26.0-0<br/><1.26.6</code></td></tr>
<tr><td>Fixed version</td><td><code>1.26.6</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.55%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>45th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

Previously, resolving relative paths containing parent directory ('..') segments performed string conversions and buffer rewrites on each step, resulting in quadratic time complexity and high memory allocation overhead.

Now, path resolution operates on a byte buffer using index-based backtracking for '..' segments, eliminating the quadratic time complexity and significantly reducing memory allocations.

</blockquote>
</details>
</details></td></tr>

<tr><td valign="top">
<details><summary><img alt="critical: 3" src="https://img.shields.io/badge/C-3-8b1924"/> <img alt="high: 14" src="https://img.shields.io/badge/H-14-e25d68"/> <img alt="medium: 4" src="https://img.shields.io/badge/M-4-fbb552"/> <img alt="low: 0" src="https://img.shields.io/badge/L-0-lightgrey"/> <!-- unspecified: 0 --><strong>stdlib</strong> <code>1.26.5</code> (golang)</summary>

<small><code>pkg:golang/stdlib@1.26.5</code></small><br/>
<a href="https://scout.docker.com/v/CVE-2026-56857?s=golang&n=stdlib&t=golang&vr=%3C1.26.9"><img alt="critical : CVE--2026--56857" src="https://img.shields.io/badge/CVE--2026--56857-lightgrey?label=critical%20&labelColor=8b1924"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.26.9</code></td></tr>
<tr><td>Fixed version</td><td><code>1.26.9</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.49%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>41st percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

On Windows, when the target of Root.Mkdir or Root.MkdirAll is a junction pointing to an empty location, the operation can create a directory at the junction target even when that target is located outside the root. This only applies to operations where the last path component is a junction (path/to/junction, but not path/junction/target).

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-39821?s=golang&n=stdlib&t=golang&vr=%3E%3D1.26.0-0%2C%3C1.26.6"><img alt="critical : CVE--2026--39821" src="https://img.shields.io/badge/CVE--2026--39821-lightgrey?label=critical%20&labelColor=8b1924"/></a> 

<table>
<tr><td>Affected range</td><td><code>>=1.26.0-0<br/><1.26.6</code></td></tr>
<tr><td>Fixed version</td><td><code>1.26.6</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.69%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>52nd percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

The ToASCII and ToUnicode functions incorrectly accept Punycode-encoded labels that decode to an ASCII-only label. For example, ToUnicode("xn--example-.com") incorrectly returns the name "example.com" rather than an error.

This behavior can lead to privilege escalation in programs using the idna package. For example, a program which performs privilege checks on the ASCII hostname may reject "example.com" but permit "xn--example-.com". If that program subsequently converts the ASCII hostname to Unicode, it will inadvertently permits access to the Unicode name "example.com".

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-78663?s=golang&n=stdlib&t=golang&vr=%3C1.26.9"><img alt="critical : CVE--2026--78663" src="https://img.shields.io/badge/CVE--2026--78663-lightgrey?label=critical%20&labelColor=8b1924"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.26.9</code></td></tr>
<tr><td>Fixed version</td><td><code>1.26.9</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.57%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>46th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

The HTTP/2 server can refund connection-level flow control twice for the same data: Once when a client resets a stream (refunding data for any sent-but-unread portion of the stream), and again when a request handler reads the buffered data. A malicious client can exploit this to bypass the configured connection-level flow control limit (MaxReceiveBufferPerConnection). Total buffered data is still limited by the concurrent stream limit and stream-level flow control.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-97032?s=golang&n=stdlib&t=golang&vr=%3C1.26.9"><img alt="high : CVE--2026--97032" src="https://img.shields.io/badge/CVE--2026--97032-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.26.9</code></td></tr>
<tr><td>Fixed version</td><td><code>1.26.9</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.42%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>35th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

HTTP/2 servers could end up crashing due to inadvertently modifying its HPACK encoder concurrently. This happens because the server modifies the HPACK encoder from two goroutines without synchronization: one uses the encoder to encode a HEADERS frame as part of a response sent to a client and the other modifies the encoder's table size when handling a SETTINGS frame containing SETTINGS_HEADER_TABLE_SIZE that a client sends. A malicious client can repeatedly send a request while changing the header table size to crash the server.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-97031?s=golang&n=stdlib&t=golang&vr=%3C1.26.9"><img alt="high : CVE--2026--97031" src="https://img.shields.io/badge/CVE--2026--97031-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.26.9</code></td></tr>
<tr><td>Fixed version</td><td><code>1.26.9</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.39%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>32nd percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

Multiple ECH outer extension references are not permitted under RFC 9849; previously, a client could send a well-crafted packet that could trigger memory exhaustion in the server process by specifying multiple references.

We now reject these as malformed and curb the memory amplification vector as a result.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-94440?s=golang&n=stdlib&t=golang&vr=%3C1.26.9"><img alt="high : CVE--2026--94440" src="https://img.shields.io/badge/CVE--2026--94440-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.26.9</code></td></tr>
<tr><td>Fixed version</td><td><code>1.26.9</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.40%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>33rd percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

Parsing a multipart form can bypass memory limits and read an arbitrarily long line into memory when the remaining limit at the start of a part is less than 400 bytes.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-94439?s=golang&n=stdlib&t=golang&vr=%3C1.26.9"><img alt="high : CVE--2026--94439" src="https://img.shields.io/badge/CVE--2026--94439-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.26.9</code></td></tr>
<tr><td>Fixed version</td><td><code>1.26.9</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.31%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>23rd percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

When an HTTP server handler sends a 2xx response to an HTTP/1 CONNECT request and returns without hijacking the connection, the server improperly continues to read and serve requests from the connection. Since a 2xx response to an HTTP/1 CONNECT converts the connection into a tunnel, the server should not treat the connection as continuing to contain HTTP.

The impact of this misbehavior is mostly limited to potential request smuggling, where an intermediate proxy considers the data on the connection to be tunneled and the server considers it to be HTTP.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-78669?s=golang&n=stdlib&t=golang&vr=%3C1.26.9"><img alt="high : CVE--2026--78669" src="https://img.shields.io/badge/CVE--2026--78669-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.26.9</code></td></tr>
<tr><td>Fixed version</td><td><code>1.26.9</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.57%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>46th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

A malicious HTTP/2 peer can cause excessive CPU consumption in the client or server by opening a large number of streams and then sending many small SETTINGS frames containing SETTINGS_INITIAL_WINDOW_SIZE values.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-78667?s=golang&n=stdlib&t=golang&vr=%3C1.26.9"><img alt="high : CVE--2026--78667" src="https://img.shields.io/badge/CVE--2026--78667-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.26.9</code></td></tr>
<tr><td>Fixed version</td><td><code>1.26.9</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.38%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>30th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

When parsing a Range header containing a large number of small ranges, FileServer(FS), ServeContent, and ServeFile(FS) can consume an excessive amount of CPU.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-78660?s=golang&n=stdlib&t=golang&vr=%3C1.26.9"><img alt="high : CVE--2026--78660" src="https://img.shields.io/badge/CVE--2026--78660-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.26.9</code></td></tr>
<tr><td>Fixed version</td><td><code>1.26.9</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.30%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>22nd percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

Historically, we have been rather lax about malformed framing-related headers in our HTTP/2 implementation, as they cannot interfere with HTTP/2 framing. However, this makes it possible for our HTTP/2 implementation to forward responses containing such headers to an HTTP/1 client when acting as a reverse proxy. If the HTTP/1 client also does not behave strictly enough, this can result in response smuggling.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-78659?s=golang&n=stdlib&t=golang&vr=%3C1.26.9"><img alt="high : CVE--2026--78659" src="https://img.shields.io/badge/CVE--2026--78659-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.26.9</code></td></tr>
<tr><td>Fixed version</td><td><code>1.26.9</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.57%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>46th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

When "Trailer" headers are sent by a client, the HTTP server internally uses the header values to populate the Request.Trailer map passed to the server handler. Because Request.Trailer is a map, each entry incurs memory overhead. For HTTP/2 servers, a malicious client can exploit this by sending a "Trailer" header that declares a large number of fields, causing the server to allocate a disproportionate amount of memory while bypassing Server.MaxHeaderValueCount and Server.MaxHeaderBytes limits. This exploit is not applicable for HTTP/1 servers, which do not support multiplexing a large number of requests over one TCP connection, and whose Server.MaxHeaderBytes are calculated differently.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-56866?s=golang&n=stdlib&t=golang&vr=%3C1.26.9"><img alt="high : CVE--2026--56866" src="https://img.shields.io/badge/CVE--2026--56866-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.26.9</code></td></tr>
<tr><td>Fixed version</td><td><code>1.26.9</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.31%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>22nd percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

When http.Transport sends an HTTP/1 CONNECT request with a non-empty Request.Body, it writes the body directly to the connection without framing after the request headers. If the server rejects the CONNECT request with a non-2xx keep-alive response, Transport returns the connection to the idle pool. Because CONNECT requests do not have a request body, the server may interpret the trailing body bytes as a subsequent pipelined HTTP/1.1 request on the connection, leaving the pooled connection desynchronized and causing the next caller that reuses it to read the response to the injected request. In reverse proxies (including httputil.ReverseProxy) that forward CONNECT requests through a shared Transport, this can lead to cross-user response poisoning.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-56862?s=golang&n=stdlib&t=golang&vr=%3E%3D1.26.0-0%2C%3C1.26.6"><img alt="high : CVE--2026--56862" src="https://img.shields.io/badge/CVE--2026--56862-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code>>=1.26.0-0<br/><1.26.6</code></td></tr>
<tr><td>Fixed version</td><td><code>1.26.6</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.57%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>46th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

Handshake messages, such as KeyUpdate, are always considered as state-advancing, regardless of whether a handshake has been completed or not. As a result, a malicious client can keep sending KeyUpdate messages to force the server to keep performing key derivation operations indefinitely.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-56859?s=golang&n=stdlib&t=golang&vr=%3E%3D1.26.0-0%2C%3C1.26.6"><img alt="high : CVE--2026--56859" src="https://img.shields.io/badge/CVE--2026--56859-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code>>=1.26.0-0<br/><1.26.6</code></td></tr>
<tr><td>Fixed version</td><td><code>1.26.6</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.57%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>46th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

Previously, DecodeElement would reset the depth counter causing it to never fire; this could lead to stack exhaustion.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-56853?s=golang&n=stdlib&t=golang&vr=%3E%3D1.26.0-0%2C%3C1.26.6"><img alt="high : CVE--2026--56853" src="https://img.shields.io/badge/CVE--2026--56853-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code>>=1.26.0-0<br/><1.26.6</code></td></tr>
<tr><td>Fixed version</td><td><code>1.26.6</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.57%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>46th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

When a server is configured to support unencrypted HTTP/2, it reads a few bytes from each new connection to see if they contain the HTTP/2 client preface. ReadHeaderTimeout is unexpectedly not being applied when doing this.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-46600?s=golang&n=stdlib&t=golang&vr=%3E%3D1.26.0-0%2C%3C1.26.6"><img alt="high : CVE--2026--46600" src="https://img.shields.io/badge/CVE--2026--46600-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code>>=1.26.0-0<br/><1.26.6</code></td></tr>
<tr><td>Fixed version</td><td><code>1.26.6</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.55%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>45th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

Parsing an invalid SVCB or HTTPS RR can panic when the size of a parameter value overflows the message buffer.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-33818?s=golang&n=stdlib&t=golang&vr=%3E%3D1.26.0-0%2C%3C1.26.6"><img alt="high : CVE--2026--33818" src="https://img.shields.io/badge/CVE--2026--33818-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code>>=1.26.0-0<br/><1.26.6</code></td></tr>
<tr><td>Fixed version</td><td><code>1.26.6</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.57%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>46th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

Enforce a recursion limit in Unmarshal to prevent stack exhaustion when parsing deeply-nested, recursive structures.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-97030?s=golang&n=stdlib&t=golang&vr=%3C1.26.9"><img alt="medium : CVE--2026--97030" src="https://img.shields.io/badge/CVE--2026--97030-lightgrey?label=medium%20&labelColor=fbb552"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.26.9</code></td></tr>
<tr><td>Fixed version</td><td><code>1.26.9</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.20%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>9th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

A trusted template author may have previously written a valid template wherein the use of the 'yield' keyword would not be correctly escaped.

We now ensure that valid keyword uses are escaped and non-keyword uses are not escaped.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-94448?s=golang&n=stdlib&t=golang&vr=%3C1.26.9"><img alt="medium : CVE--2026--94448" src="https://img.shields.io/badge/CVE--2026--94448-lightgrey?label=medium%20&labelColor=fbb552"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.26.9</code></td></tr>
<tr><td>Fixed version</td><td><code>1.26.9</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.20%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>9th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

When a JavaScript template literal contains consecutive expressions, the context tracking state was not properly reset upon entering a new expression.

We now ensure that template-literal expression entries correctly reset context variables so all subsequent regular expression literals are accurately recognized and escaped.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-56858?s=golang&n=stdlib&t=golang&vr=%3E%3D1.26.0-0%2C%3C1.26.6"><img alt="medium : CVE--2026--56858" src="https://img.shields.io/badge/CVE--2026--56858-lightgrey?label=medium%20&labelColor=fbb552"/></a> 

<table>
<tr><td>Affected range</td><td><code>>=1.26.0-0<br/><1.26.6</code></td></tr>
<tr><td>Fixed version</td><td><code>1.26.6</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.31%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>22nd percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

Previously, pathological inputs could close an unescaped '/' early, allowing for attack-controlled data to inject arbitrary content, potentially leading to XSS.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-56860?s=golang&n=stdlib&t=golang&vr=%3E%3D1.26.0-0%2C%3C1.26.6"><img alt="medium : CVE--2026--56860" src="https://img.shields.io/badge/CVE--2026--56860-lightgrey?label=medium%20&labelColor=fbb552"/></a> 

<table>
<tr><td>Affected range</td><td><code>>=1.26.0-0<br/><1.26.6</code></td></tr>
<tr><td>Fixed version</td><td><code>1.26.6</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.55%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>45th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

Previously, resolving relative paths containing parent directory ('..') segments performed string conversions and buffer rewrites on each step, resulting in quadratic time complexity and high memory allocation overhead.

Now, path resolution operates on a byte buffer using index-based backtracking for '..' segments, eliminating the quadratic time complexity and significantly reducing memory allocations.

</blockquote>
</details>
</details></td></tr>

<tr><td valign="top">
<details><summary><img alt="critical: 1" src="https://img.shields.io/badge/C-1-8b1924"/> <img alt="high: 5" src="https://img.shields.io/badge/H-5-e25d68"/> <img alt="medium: 0" src="https://img.shields.io/badge/M-0-lightgrey"/> <img alt="low: 0" src="https://img.shields.io/badge/L-0-lightgrey"/> <!-- unspecified: 0 --><strong>golang.org/x/net</strong> <code>0.55.0</code> (golang)</summary>

<small><code>pkg:golang/golang.org/x/net@0.55.0</code></small><br/>
<a href="https://scout.docker.com/v/CVE-2026-78663?s=golang&n=net&ns=golang.org%2Fx&t=golang&vr=%3C0.60.0"><img alt="critical : CVE--2026--78663" src="https://img.shields.io/badge/CVE--2026--78663-lightgrey?label=critical%20&labelColor=8b1924"/></a> 

<table>
<tr><td>Affected range</td><td><code><0.60.0</code></td></tr>
<tr><td>Fixed version</td><td><code>0.60.0</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.57%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>46th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

The HTTP/2 server can refund connection-level flow control twice for the same data: Once when a client resets a stream (refunding data for any sent-but-unread portion of the stream), and again when a request handler reads the buffered data. A malicious client can exploit this to bypass the configured connection-level flow control limit (MaxReceiveBufferPerConnection). Total buffered data is still limited by the concurrent stream limit and stream-level flow control.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-97032?s=golang&n=net&ns=golang.org%2Fx&t=golang&vr=%3C0.60.0"><img alt="high : CVE--2026--97032" src="https://img.shields.io/badge/CVE--2026--97032-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code><0.60.0</code></td></tr>
<tr><td>Fixed version</td><td><code>0.60.0</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.42%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>35th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

HTTP/2 servers could end up crashing due to inadvertently modifying its HPACK encoder concurrently. This happens because the server modifies the HPACK encoder from two goroutines without synchronization: one uses the encoder to encode a HEADERS frame as part of a response sent to a client and the other modifies the encoder's table size when handling a SETTINGS frame containing SETTINGS_HEADER_TABLE_SIZE that a client sends. A malicious client can repeatedly send a request while changing the header table size to crash the server.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-78669?s=golang&n=net&ns=golang.org%2Fx&t=golang&vr=%3C0.60.0"><img alt="high : CVE--2026--78669" src="https://img.shields.io/badge/CVE--2026--78669-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code><0.60.0</code></td></tr>
<tr><td>Fixed version</td><td><code>0.60.0</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.57%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>46th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

A malicious HTTP/2 peer can cause excessive CPU consumption in the client or server by opening a large number of streams and then sending many small SETTINGS frames containing SETTINGS_INITIAL_WINDOW_SIZE values.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-78660?s=golang&n=net&ns=golang.org%2Fx&t=golang&vr=%3C0.60.0"><img alt="high : CVE--2026--78660" src="https://img.shields.io/badge/CVE--2026--78660-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code><0.60.0</code></td></tr>
<tr><td>Fixed version</td><td><code>0.60.0</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.30%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>22nd percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

Historically, we have been rather lax about malformed framing-related headers in our HTTP/2 implementation, as they cannot interfere with HTTP/2 framing. However, this makes it possible for our HTTP/2 implementation to forward responses containing such headers to an HTTP/1 client when acting as a reverse proxy. If the HTTP/1 client also does not behave strictly enough, this can result in response smuggling.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-78659?s=golang&n=net&ns=golang.org%2Fx&t=golang&vr=%3C0.60.0"><img alt="high : CVE--2026--78659" src="https://img.shields.io/badge/CVE--2026--78659-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code><0.60.0</code></td></tr>
<tr><td>Fixed version</td><td><code>0.60.0</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.57%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>46th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

When "Trailer" headers are sent by a client, the HTTP server internally uses the header values to populate the Request.Trailer map passed to the server handler. Because Request.Trailer is a map, each entry incurs memory overhead. For HTTP/2 servers, a malicious client can exploit this by sending a "Trailer" header that declares a large number of fields, causing the server to allocate a disproportionate amount of memory while bypassing Server.MaxHeaderValueCount and Server.MaxHeaderBytes limits. This exploit is not applicable for HTTP/1 servers, which do not support multiplexing a large number of requests over one TCP connection, and whose Server.MaxHeaderBytes are calculated differently.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-46600?s=golang&n=net&ns=golang.org%2Fx&t=golang&vr=%3C0.56.0"><img alt="high : CVE--2026--46600" src="https://img.shields.io/badge/CVE--2026--46600-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code><0.56.0</code></td></tr>
<tr><td>Fixed version</td><td><code>0.56.0</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.55%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>45th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

Parsing an invalid SVCB or HTTPS RR can panic when the size of a parameter value overflows the message buffer.

</blockquote>
</details>
</details></td></tr>

<tr><td valign="top">
<details><summary><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 3" src="https://img.shields.io/badge/H-3-e25d68"/> <img alt="medium: 0" src="https://img.shields.io/badge/M-0-lightgrey"/> <img alt="low: 0" src="https://img.shields.io/badge/L-0-lightgrey"/> <img alt="unspecified: 1" src="https://img.shields.io/badge/U-1-lightgrey"/><strong>golang.org/x/crypto</strong> <code>0.53.0</code> (golang)</summary>

<small><code>pkg:golang/golang.org/x/crypto@0.53.0</code></small><br/>
<a href="https://scout.docker.com/v/CVE-2026-78662?s=golang&n=crypto&ns=golang.org%2Fx&t=golang&vr=%3C0.56.0"><img alt="high : CVE--2026--78662" src="https://img.shields.io/badge/CVE--2026--78662-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code><0.56.0</code></td></tr>
<tr><td>Fixed version</td><td><code>0.56.0</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.43%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>36th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

Previously, a channel registered in the mux's chanList is not usable until it is established. A malicious peer was able flood the channel's incomingRequests, deadlocking the entire connection.

Now, we add an atomic established state, set when a channel becomes usable. Until such a time, handlePacket drops every packet other than the open confirmation/failure, without blocking and without tearing down the connection.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-56855?s=golang&n=crypto&ns=golang.org%2Fx&t=golang&vr=%3C0.56.0"><img alt="high : CVE--2026--56855" src="https://img.shields.io/badge/CVE--2026--56855-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code><0.56.0</code></td></tr>
<tr><td>Fixed version</td><td><code>0.56.0</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.50%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>41st percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

Previously, after a channel has been established, a malicious peer could send crafted messages that would deadlock the entire connection.

Now, we handle all RFC 4254 channel messages; global requests are handled explicitly. Then, treat all other messages as a protocol error and tear the connection down instead of buffering and blocking.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-56854?s=golang&n=crypto&ns=golang.org%2Fx&t=golang&vr=%3C0.55.0"><img alt="high : CVE--2026--56854" src="https://img.shields.io/badge/CVE--2026--56854-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code><0.55.0</code></td></tr>
<tr><td>Fixed version</td><td><code>0.55.0</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.44%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>37th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

The source-address critical option in the Permissions returned by an authentication callback was only enforced for the PublicKeyCallback and VerifiedPublicKeyCallback paths, extending the fix for CVE-2026-46595. Permissions returned by the PasswordCallback, KeyboardInteractiveCallback, NoClientAuthCallback, and GSSAPIWithMICConfig.AllowLogin callbacks were not validated against the client's remote address, so a source-address restriction set by those callbacks was silently ignored. The check is now applied to the Permissions returned by any authentication callback.

</blockquote>
</details>

<a href="https://scout.docker.com/v/GO-2026-5932?s=golang&n=crypto&ns=golang.org%2Fx&t=golang&vr=%3E%3D0"><img alt="unspecified : GO--2026--5932" src="https://img.shields.io/badge/GO--2026--5932-lightgrey?label=unspecified%20&labelColor=lightgrey"/></a> 

<table>
<tr><td>Affected range</td><td><code>>=0</code></td></tr>
<tr><td>Fixed version</td><td><strong>Not Fixed</strong></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

The golang.org/x/crypto/openpgp package is unsafe by design, has numerous known security issues, is not maintained, and should not be used.

If you are required to interoperate with OpenPGP systems and need a maintained package, consider github.com/ProtonMail/go-crypto/openpgp which is a maintained fork that aims to be a drop-in replacement for this package.

</blockquote>
</details>
</details></td></tr>

<tr><td valign="top">
<details><summary><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 1" src="https://img.shields.io/badge/H-1-e25d68"/> <img alt="medium: 0" src="https://img.shields.io/badge/M-0-lightgrey"/> <img alt="low: 0" src="https://img.shields.io/badge/L-0-lightgrey"/> <img alt="unspecified: 1" src="https://img.shields.io/badge/U-1-lightgrey"/><strong>golang.org/x/text</strong> <code>0.38.0</code> (golang)</summary>

<small><code>pkg:golang/golang.org/x/text@0.38.0</code></small><br/>
<a href="https://scout.docker.com/v/CVE-2026-56851?s=golang&n=text&ns=golang.org%2Fx&t=golang&vr=%3C0.41.0"><img alt="high : CVE--2026--56851" src="https://img.shields.io/badge/CVE--2026--56851-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code><0.41.0</code></td></tr>
<tr><td>Fixed version</td><td><code>0.41.0</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.33%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>25th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

The Nickname profile can panic with an out-of-bounds slice error when transforming crafted input into a short destination buffer.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-56852?s=golang&n=text&ns=golang.org%2Fx&t=golang&vr=%3C0.39.0"><img alt="unspecified : CVE--2026--56852" src="https://img.shields.io/badge/CVE--2026--56852-lightgrey?label=unspecified%20&labelColor=lightgrey"/></a> 

<table>
<tr><td>Affected range</td><td><code><0.39.0</code></td></tr>
<tr><td>Fixed version</td><td><code>0.39.0</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.47%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>40th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

A norm.Iter can enter an infinite loop when handling input containing invalid UTF-8 bytes.

</blockquote>
</details>
</details></td></tr>
</table>

