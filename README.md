# TCP SYN Flood Incident Report

> **Category:** Network Security • **Attack Type:** Denial of Service (DoS)  
> **Objective:** Analyze and document a SYN Flood attack detected on the company web server.  

---

## Overview
A sudden spike in **TCP SYN packets** from IP `203.0.113.0` overwhelmed the travel agency’s web server, resulting in **connection timeouts** and **website unavailability**.  
The attacker exploited the TCP three-way handshake to exhaust server resources — a classic **SYN Flood Attack**.

---

## Evidence Summary
| Observation | Detail |
|--------------|---------|
| **Protocol** | TCP |
| **Target Port** | 443 (HTTPS) |
| **Source IP** | `203.0.113.0` |
| **Symptoms** | Half-open connections, 504 Gateway Timeouts |
| **Captured by** | Packet Sniffer / Wireshark |
| **Pattern** | Continuous SYN requests with no ACK response |

---

## Impact
- Website became **unreachable** for employees and customers.  
- Caused **loss of service availability** and potential **revenue impact**.  
- Server resources maxed out, leading to **slow response** and **timeouts**.  
- Potential distraction for **secondary attacks** or **reconnaissance**.

---

## Mitigation & Recommendations
- **Enable SYN Cookies** to handle half-open connections efficiently.  
- **Rate-limit incoming SYN requests** using firewalls or load balancers.  
- Deploy **IDS/IPS** (Intrusion Detection/Prevention Systems).  
- Use **Cloud DDoS Mitigation Services** like Cloudflare or AWS Shield.  
- Block or throttle suspicious IPs temporarily.
