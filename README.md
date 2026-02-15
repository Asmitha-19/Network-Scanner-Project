# 🔎 Network Scanning Project using Nmap

## 📘 Introduction

This project focuses on practical network reconnaissance using Nmap in a Kali Linux virtual lab environment. The goal is to analyze network devices, identify exposed services, and understand how attackers and security professionals gather information about systems.

Network scanning is one of the most important phases in cybersecurity assessment and penetration testing.

---

## 🎯 Project Goals

- Discover active hosts in a network
- Identify open TCP and UDP ports
- Detect running services and their versions
- Perform operating system fingerprinting
- Apply stealth and evasion scanning techniques
- Evaluate potential security risks

---

## 🛠 Lab Environment

**Operating System:** Kali Linux  
**Scanning Tool:** Nmap  
**Virtualization Platform:** VMware  
**Host Machine:** Windows  

### Setup Steps
1. Installed VMware on Windows host.
2. Installed and configured Kali Linux virtual machine.
3. Verified network connectivity using `ip a`.
4. Confirmed Nmap installation before scanning.

---

# 🚀 Practical Implementation

---

## 🔹 Basic Information Gathering

### Check Nmap Installation
```bash
nmap --version
Scan Single Target
nmap 10.85.57.71


Performs default scan on top 1000 TCP ports.

Scan a Website
nmap example.com


Resolves domain name and scans associated IP address.

Scan Entire Subnet
nmap 10.85.57.0/24


Scans all hosts within the specified network range.

Discover Active Hosts Only
nmap -sn 10.85.57.0/24


Performs host discovery without port scanning.

🔹 Port Scanning Techniques
Scan Specific Port
nmap -p 80 10.198.101.71


Checks availability of HTTP service.

Scan Multiple Ports
nmap -p 22,80,443 10.198.101.71


Scans commonly used service ports.

Scan Port Range
nmap -p 1-1000 10.198.101.71


Scans first 1000 TCP ports.

Scan All TCP Ports
nmap -p- 10.198.101.71


Scans all 65535 TCP ports.

🔹 Service & Version Detection
Service Version Detection
nmap -sV 10.198.101.71


Identifies service names and exact versions.

Light Version Scan
nmap -sV --version-light 10.198.101.71


Faster version detection using limited probes.

🔹 Operating System Detection
Basic OS Detection
nmap -O 10.198.101.71


Attempts to identify operating system.

Aggressive OS Guess
nmap -O --osscan-guess 10.198.101.71


Provides best possible OS guess if uncertain.

🔹 Scan Types
SYN (Stealth) Scan
nmap -sS 10.198.101.71


Half-open scan; less likely to be logged.

TCP Connect Scan
nmap -sT 10.198.101.71


Full connection scan visible in logs.

UDP Scan
nmap -sU 10.198.101.71


Detects UDP-based services.

FIN Scan
nmap -sF 10.198.101.71


Firewall evasion technique using FIN packets.

NULL Scan
nmap -sN 10.198.101.71


Sends packets with no TCP flags set.

Xmas Scan
nmap -sX 10.198.101.71


Uses FIN, PSH, and URG flags combination.

🔹 Advanced Scanning
Aggressive Scan
nmap -A 10.198.101.71


Combines OS detection, version detection, scripts, and traceroute.

Traceroute
nmap --traceroute 10.198.101.71


Shows network path between scanner and target.

Fragmented Packets
nmap -f 10.198.101.71


Splits packets to bypass basic filters.

Decoy Scan
nmap -D RND:5 10.198.101.71


Uses random decoy IP addresses to hide scanner identity.

Spoof MAC Address
nmap --spoof-mac random 10.198.101.71


Changes MAC address for local network evasion.

🔹 NSE Script Scanning
Default Script Scan
nmap -sC 10.198.101.71


Runs default safe Nmap scripts.

Vulnerability Scan
nmap --script vuln 10.198.101.71


Checks for known vulnerabilities.

Specific Script Example
nmap --script http-title 10.198.101.71


Extracts web page title from HTTP service.

Faster Scan Timing
nmap -T4 10.198.101.71


Speeds up scan using aggressive timing template.

📊 Observations

Open ports increase attack surface.

Outdated services may lead to vulnerabilities.

Firewall rules affect scan visibility.

Stealth scans reduce logging probability.

🛡 Security Recommendations

Close unused ports.

Update outdated services.

Enable firewall filtering.

Monitor suspicious network activity.

Conduct periodic security assessments.

📌 Conclusion

This project provided hands-on exposure to real-world network scanning techniques. Through multiple Nmap scan types, it was possible to understand host discovery, service enumeration, OS detection, and security risk evaluation.

The practical experience gained from this project strengthens foundational knowledge in cybersecurity and penetration testing.

👨‍💻 Author

ASMITHA 
Cybersecurity Student
