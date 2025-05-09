# Common Obfuscation Techniques in XSS Attacks

| Technique               | Example                                         | Purpose                              |
|------------------------|-------------------------------------------------|--------------------------------------|
| Simple URL encoding    | `%3Cscript%3E`                                  | Escape special characters            |
| Double encoding        | `%253Cscript%253E`                              | Bypass single-layer decoders         |
| HTML entities          | `&lt;script&gt;`                                | Prevent HTML rendering               |
| Unicode encoding       | `\u003Cscript\u003E`                          | Bypass Unicode parsers               |
| Hex encoding (JS)      | `\x3Cscript\x3E`                              | Obfuscate in JS context              |
| Base64 encoding        | `PHNjcmlwdD5hbGVydCgpPC9zY3JpcHQ+`             | Hide complete payload                |
| Mixed encoding         | Mix of `%`, `&lt;`, `\u...`                   | Evade regex-based filters            |
| Whitespace obfuscation | `<scr ipt>alert(1)</scr ipt>`                   | Break detection logic                |
| Comment injection      | `<script><!--alert(1);//--></script>`           | Split malicious code                 |
