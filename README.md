# homelab-segmented-network
Home Lab segmentation documentation
# 🔐 Segmented Home Lab Network — Zero-Trust Architecture  
*A professional-grade VLAN-based network for cybersecurity research and homelab engineering.*

![Status](https://img.shields.io/badge/status-complete-brightgreen)
![MikroTik](https://img.shields.io/badge/router-mikrotik-blue)
![Cisco](https://img.shields.io/badge/switch-cisco%20catalyst-blue)
![Security](https://img.shields.io/badge/security-zero--trust-critical)
![Docs](https://img.shields.io/badge/documentation-extensive-success)

---

## 📘 Overview

This project documents the full design and implementation of a **multi-VLAN, zero-trust–inspired home lab network** using:

- **MikroTik hEX Lite** (router/firewall)
- **Cisco Catalyst 2950** (Layer-2 switching)
- **TP-Link SG108E** (secondary VLAN switch)
- **Eero mesh system** (WAN gateway)
- **Linux NAS** (Plex + storage server)
- **Windows & Linux workstations**
- **IoT devices**

The goal was to build a secure, enterprise-style segmented network suitable for:

- Cybersecurity practice  
- Linux server hosting  
- Virtualization  
- Research  
- Portfolio demonstration  

This repository includes all documentation, diagrams, configurations, and validation steps.

---

## 🏛️ Architecture Summary

This home lab uses a **Router-on-a-Stick design** with the MikroTik as the L3 core and the Cisco Catalyst providing VLAN access switching.

### ✅ VLANs

| VLAN | Purpose | Subnet |
|------|---------|--------|
| 10 | Trusted Workstations | 10.10.10.0/24 |
| 20 | NAS / Servers | 10.10.20.0/24 |
| 40 | IoT Network | 10.10.40.0/24 |
| 99 | Management | 10.10.99.0/24 |

### ✅ Key Security Principles Implemented

- **Default-deny firewall**  
- **Least-privilege inter-VLAN access**  
- **NAS isolation from all networks except trusted workstation**  
- **IoT → Internet only**  
- **Management VLAN restricted to trusted host**  
- **Logging, monitoring, and future VPN support**  

---

## 🧩 Logical Network Diagram

(Place your diagram here, or use your `/docs/diagrams/logical.png`.)

