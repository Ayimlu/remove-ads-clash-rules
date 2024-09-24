```
dns:
  fake-ip-filter:
    - "rule-set:ultimate"
    - "rule-set:popupads"
    - "rule-set:doh-vpn-proxy-bypass"
  nameserver-policy:
    "rule-set:ultimate": rcode://success
    "rule-set:popupads": rcode://success
    "rule-set:doh-vpn-proxy-bypass": rcode://success
rule-providers:
  ultimate:
    type: http
    interval: 86400
    format: yaml
    behavior: domain
    url: "https://raw.githubusercontent.com/Ayimlu/remove-ads-clash-rules/refs/heads/main/ultimate.txt"
  popupads:
    type: http
    interval: 86400
    format: yaml
    behavior: domain
    url: "https://raw.githubusercontent.com/Ayimlu/remove-ads-clash-rules/refs/heads/main/popupads.txt"
  doh-vpn-proxy-bypass:
    type: http
    interval: 86400
    format: yaml
    behavior: domain
    url: "https://raw.githubusercontent.com/Ayimlu/remove-ads-clash-rules/refs/heads/main/doh-vpn-proxy-bypass.txt"
```
