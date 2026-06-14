# 🌐 Network_Task_02_YourName

> **Internship Networking Task 02** — Network Devices & IP Addressing  
> Replace `YourName` in the folder name with your actual name before submission.

---

## 📋 Table of Contents

- [Overview](#overview)
- [Folder Structure](#folder-structure)
- [Part A – Network Devices](#part-a--network-devices)
- [Part B – IP Address Classification](#part-b--ip-address-classification)
- [Part C – Understanding Your Network](#part-c--understanding-your-network)
- [Part D – Network Communication Flow](#part-d--network-communication-flow)
- [Part E – Practical Command Exercise](#part-e--practical-command-exercise)
- [Key Learnings](#key-learnings)
- [Tools & Commands Used](#tools--commands-used)

---

## 📌 Overview

This task covers the fundamentals of networking including common network devices, IP address classification (Public vs Private), practical command-line tools, and understanding how data flows across a network when a website is accessed.

---

## 📁 Folder Structure

```
Network_Task_02_YourName/
│
├── README.md                  # This file
├── answers.md                 # Written answers for all parts
│
├── screenshots/
│   ├── ipconfig_all.png       # Output of ipconfig /all (or ip addr)
│   ├── nslookup_google.png    # Output of nslookup google.com
│   └── ping_google.png        # Output of ping google.com
│
└── network_diagram/
    └── communication_flow.png # Diagram for Part D
```

---

## Part A – Network Devices

Researched and explained the following devices in `answers.md`:

| Device | Purpose |
|---|---|
| **Router** | Connects different networks; routes packets between LAN and internet |
| **Switch** | Connects devices within a LAN; forwards frames using MAC addresses |
| **Hub** | Broadcasts data to all ports; obsolete, replaced by switches |
| **Access Point** | Provides wireless (Wi-Fi) connectivity by bridging wired and wireless networks |
| **Firewall** | Filters traffic based on rules; protects network from unauthorized access |
| **Modem** | Converts digital signals to/from the format used by ISP infrastructure |

---

## Part B – IP Address Classification

| IP Address | Type | Reason |
|---|---|---|
| `192.168.1.10` | 🔒 Private | RFC 1918 — 192.168.0.0/16 range |
| `10.0.0.5` | 🔒 Private | RFC 1918 — 10.0.0.0/8 range |
| `172.16.5.20` | 🔒 Private | RFC 1918 — 172.16.0.0/12 range |
| `8.8.8.8` | 🌐 Public | Google DNS — globally routable |
| `1.1.1.1` | 🌐 Public | Cloudflare DNS — globally routable |
| `192.168.100.1` | 🔒 Private | RFC 1918 — 192.168.0.0/16 range |

---

## Part C – Understanding Your Network

Commands run on personal device to retrieve network information.  
*(See screenshots folder for command outputs)*

- **IPv4 Address:** `[your device IP]`
- **Default Gateway:** `[your router IP]`
- **DNS Server:** `[your DNS IP]`
- **IP Range:** Private (192.168.x.x)
- **Router Role:** Acts as the default gateway, performs NAT, and manages DHCP for the local network.
- **If DNS stopped working:** Domain name resolution would fail — websites would be unreachable by name even if the internet connection is active.

---

## Part D – Network Communication Flow

Diagram located at: `network_diagram/communication_flow.png`

```
Your Device
    ↓  (DNS query: what is google.com's IP?)
Router (Default Gateway)
    ↓
ISP Network
    ↓
DNS Server  →  returns IP e.g. 142.250.77.46
    ↓
Google's Web Server
    ↓
Response travels back → ISP → Router → Your Device
    ↓
Browser renders the webpage
```

---

## Part E – Practical Command Exercise

Commands run and documented with screenshots:

### Windows
```bash
ipconfig /all
nslookup google.com
ping google.com
```

### Linux
```bash
ip addr
nslookup google.com
ping google.com
```

**Findings:**
- **DNS returned IP for Google:** `[fill in from your nslookup output]`
- **Ping successful:** Yes — received replies with TTL and response time
- **Why DNS matters:** Without DNS resolving the domain to an IP first, the device has no destination address to send the HTTP request to. DNS is the first step in almost every internet communication.

---

## 💡 Key Learnings

- Routers, switches, hubs, and access points serve different roles at different OSI layers
- Private IP ranges (RFC 1918) are not routable on the public internet — NAT bridges the gap
- DNS is a critical prerequisite to web communication — it translates names to IPs
- The `ipconfig`, `ping`, and `nslookup` commands are essential diagnostic tools for any network troubleshooter
- Every web request involves multiple network hops: device → router → ISP → DNS → destination server

---

## 🛠️ Tools & Commands Used

| Tool | Purpose |
|---|---|
| `ipconfig /all` | View IP address, gateway, DNS on Windows |
| `ip addr` | View IP configuration on Linux |
| `nslookup google.com` | Query DNS resolution for a domain |
| `ping google.com` | Test network connectivity and latency |
| Draw.io / Canva | Network diagram creation |

---

## 📤 Submission

- GitHub Repository: `[paste your repo link here]`
- Submitted via: Sunday Submission Form
- Task folder organized inside the main internship repository

---

*Part of an ongoing internship program. Each task is maintained in a separate folder within the same repository.*
