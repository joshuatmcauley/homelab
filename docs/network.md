Network:
Flat home LAN. The TL-SG108S is unmanaged: no VLANs, no trunks, no ACLs on this switch. Everything on the switch is one broadcast domain.

Path:
BT Hub (router, DHCP, Wi-Fi, gateway 192.168.1.254)
  → Wi-Fi → BT Smart Disk (extender)
  → Ethernet → TL-SG108S
  → Raspberry Pi 5
  → Windows PC 

Pi also has a 1TB SSD on USB which acts as the primary storage

What each box does:
- BT Hub — WAN, DHCP, default gateway, DNS for the house (bthub.home)
- BT Smart Disk — Wi-Fi back to the hub, Ethernet out to the switch
- TL-SG108S — 8 dumb ports, layer 2 only
- Pi 5 — homelab host (Docker / media stack)
- Windows PC — daily PC

Switch ports:
- Port 1: BT Smart disk 2
- Port 2: Raspberry Pi 5
- Port 3: Thinkpad T14
- Port 4: Windows PC
- Port 5: Empty
- Port 6: Empty
- Port 7: Empty
- Port 8: Empty


Addresses:
- Gateway / DHCP / DNS: 192.168.1.254 (hub)
- Windows Ethernet: 192.168.1.103 
- Windows Wi-Fi: 192.168.1.142
- Pi: 

