### View tunnel secret in plain text
Navigate to https://insertyourfortigateip:port/api/v2/cmdb/vpn.ipsec/phase1-interface?plain-text-password=1

PSK for IPSec Phase 1 will be displayed in plain text under psksecret

### IKE Debugging:
Use "diagnose debug application ike -1" and "diagnose debug enable" to capture detailed logs

### View status of Phase 1 and 2 
Phase 1: "diagnose vpn ike gateway list" 

Phase 2: "diagnose vpn tunnel list"

### Clear IKE sessions
All Phase 1: "diagnose vpn ike gateway clear"

All Phase 2: "diagnose vpn tunnel flush"

Add the name of the single tunnel you want to flush at the end of the command otherwise all tunnels will be flushed.

### 
