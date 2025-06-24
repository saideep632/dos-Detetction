# dos-Detetction
🛡️ Denial of Service (DoS) Attack Analysis – Project Report
📄 Overview
This project investigates a potential Denial of Service (DoS) attack scenario through system logs, network captures, and command-line tools. It primarily focuses on identifying SYN flood indicators using tools like hping3, Wireshark, and netstat.

🔍 Objective
To detect, analyze, and interpret evidence of a DoS attack (specifically SYN flooding) on a target machine using real-world tools and data.

🧪 Tools & Environment
Operating System: Windows 7

hping3 – SYN flood simulation

Wireshark – Network traffic capture and analysis

netstat – Active connection and port status viewer

📊 Evidence Summary
Source	Key Insight
System Monitor	Baseline system performance (no high load observed)
hping3	Attempted SYN flood command to 192.168.240.131 on port 80
Wireshark	Multiple TCP SYN packets without ACKs to 192.168.19.18 — classic SYN flood signature
netstat	Many TIME_WAIT states and an established connection from suspected attacker

🔎 Findings
A potential SYN flood attack is indicated from IP 192.168.240.131 to 192.168.19.18.

The use of hping3 suggests an intentional generation of traffic.

Wireshark confirms multiple half-open TCP connections.

netstat supports the pattern typical of DoS impacts on target services.

🧰 Tools Breakdown
hping3 — TCP SYN packet generator

Wireshark — Protocol-level packet analysis

netstat — Session-level connection state viewer

🧪 Recommendations for Future Work
Monitor service availability on the target machine

Capture traffic over a longer period to confirm traffic consistency

Implement basic firewall or SYN flood protection mechanisms for testing

📌 Conclusion
This analysis demonstrates how a SYN flood attack can be simulated and identified using basic tools. It highlights the importance of network visibility and log analysis in detecting DoS behaviors before they impact system availability.

