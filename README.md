# local-network-port-scanning
This project demonstrates basic network reconnaissance by scanning a local subnet to identify active hosts and open TCP ports. The goal is to understand network exposure, detect running services, and assess potential security risks associated with exposed ports.
Here is a ready-to-copy README.md content for your GitHub repository:

🔍 Local Network Port Scanning & Service Exposure Analysis
📌 Project Overview

This project focuses on performing network reconnaissance within a local subnet to identify active hosts and open TCP ports. The objective is to understand network exposure, detect running services, and assess potential security risks associated with exposed ports.

🎯 Objective

Discover open ports on devices in a local network

Identify services running on those ports

Analyze potential security risks

Document findings for security assessment

🛠 Tools Used

Nmap – Network scanning and port enumeration

Wireshark (Optional) – Packet capture and traffic analysis

🚀 Methodology
1️⃣ Identify Local Network Range

Used system network configuration (e.g., ipconfig or ip a) to determine subnet range such as:

192.168.230.132
2️⃣ Perform TCP SYN Scan
nmap -sS 192.168.230.132

This scan identifies open TCP ports without completing the full TCP handshake.

3️⃣ Analyze Scan Results

Recorded active hosts

Noted open ports and associated services

Researched common services (SSH, HTTP, HTTPS, SMB, etc.)

4️⃣ Packet Analysis (Optional)

Used Wireshark to capture packets during scanning.

Filter applied:

tcp.flags.syn == 1

Observed SYN, SYN-ACK, and RST packets to understand how open and closed ports respond.

🔎 Common Ports Identified
Port	Service	Risk
22	SSH	Brute-force attacks
80	HTTP	Web vulnerabilities
443	HTTPS	SSL misconfiguration
445	SMB	Ransomware exploits
🛡 Security Recommendations

Close unused ports

Disable unnecessary services

Configure firewall rules

Use strong passwords

Keep systems patched and updated

🎓 Learning Outcomes

Understanding of TCP three-way handshake

Hands-on experience with Nmap

Basic network reconnaissance skills

Service enumeration and risk analysis

Exposure assessment and documentation

📁 Project Structure
Local-Network-Port-Scanning/
│
├── README.md
├── scan_results.txt
├── scan.xml
└── screenshots/

Skills Demonstrated:
Network Reconnaissance | Port Scanning | TCP/IP | Nmap | Wireshark | Basic Threat Analysis
