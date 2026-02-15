---
layout: page
title: Runbooks
permalink: /runbooks.html
---

# Runbooks

## Proxmox Web UI TLS Recovery
Symptoms: can't reach :8006, cert/key errors  
Fix:
1. `rm -f /etc/pve/local/pve-ssl.pem /etc/pve/local/pve-ssl.key`
2. `pvecm updatecerts --force`
3. `systemctl restart pveproxy`

## Jump Box Autostart
- Set jump VM to start at boot
- Order: 1, Delay: 30s

## OPNsense CA Trust on Clients
- Export Root CA
- Install to OS trust store
- iOS: enable **Full Trust** in Certificate Trust Settings
