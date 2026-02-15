---
layout: page
title: Architecture
permalink: /architecture.html
---

# Architecture

## Current Topology
- **Proxmox Host:** runs core VMs/LXCs (OPNsense, Docker VM, jump box, monitoring)
- **OPNsense VM:** WAN/LAN interfaces, VLANs, firewall policies, internal CA
- **Services:** Pi-hole, Vaultwarden, monitoring stack

## Network Segments (example)
- **MGMT VLAN:** Proxmox, OPNsense admin, jump box
- **SERVERS VLAN:** Docker VM, internal services
- **CLIENTS VLAN:** laptops/phones/IoT

## Security Controls
- Default deny between VLANs
- Admin access only from MGMT
- DNS filtering + logging
- HTTPS internal PKI

(Add a diagram image here later: `assets/diagrams/topology.png`)
