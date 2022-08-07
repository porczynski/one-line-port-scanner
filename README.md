# one-line-port-scanner
Scan IP addresses in the network &amp; scan open ports with no dependencies with one-line pure linux shell code


scan with `ping` & `sh` only:
usage:
``` sh
net="192.168.1."; port=22; for ip in $(seq 1 254); do (ping $net$ip -c 1 -w 5  >/dev/null && timeout 0.2 sh -c "</dev/tcp/$net$ip/$port && echo $net$ip:$port open" 2>/dev/null &); done
```

ping




scan with `netcat`
``` sh

```
