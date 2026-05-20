<h1 align="center">SOC-Based Network Attack Detection & Traffic Analysis</h1>

<p align="center">

<img src="https://img.shields.io/badge/Wireshark-Network%20Analysis-blue?style=for-the-badge&logo=wireshark">

<img src="https://img.shields.io/badge/Nmap-Reconnaissance-darkgreen?style=for-the-badge">

<img src="https://img.shields.io/badge/Hydra-Brute%20Force-red?style=for-the-badge">

<img src="https://img.shields.io/badge/SOC-Detection%20Lab-black?style=for-the-badge">

<img src="https://img.shields.io/badge/MITRE-ATT%26CK-orange?style=for-the-badge">

</p>

<p align="center">
  <b>Cybersecurity Project</b> • Wireshark • Nmap • Hydra • SOC Analysis
</p>

<hr>

<h2>📌 Project Overview</h2>

<p>
This project demonstrates a SOC-style network attack detection lab using Kali Linux,
Windows 10, Wireshark, Nmap, Hydra, and VMware.
</p>

<p>
The objective of this project was to simulate real-world attacker behavior and analyze
network traffic generated during different phases of a cyber attack.
</p>

<p>The project includes:</p>

<ul>
  <li>ICMP reconnaissance detection</li>
  <li>TCP SYN scan analysis</li>
  <li>Service enumeration detection</li>
  <li>RDP brute force attack simulation</li>
  <li>Packet-level traffic investigation</li>
  <li>SOC investigation workflow</li>
  <li>MITRE ATT&CK mapping</li>
</ul>

<hr>

<h2>🛠️ Tools & Technologies</h2>

<table>
  <tr>
    <th>Tool</th>
    <th>Purpose</th>
  </tr>
  <tr>
    <td>Wireshark</td>
    <td>Packet analysis</td>
  </tr>
  <tr>
    <td>Kali Linux</td>
    <td>Attacker machine</td>
  </tr>
  <tr>
    <td>Windows 10</td>
    <td>Victim machine</td>
  </tr>
  <tr>
    <td>Nmap</td>
    <td>Reconnaissance and enumeration</td>
  </tr>
  <tr>
    <td>Hydra</td>
    <td>RDP brute force simulation</td>
  </tr>
  <tr>
    <td>VMware Workstation</td>
    <td>Virtual lab environment</td>
  </tr>
</table>

<hr>

<hr>

<h2>🧭 Attack Workflow</h2>

<p>
This project simulated a complete attacker reconnaissance and intrusion workflow
inside an isolated VMware lab environment.
</p>

<pre>
Attacker Reconnaissance
        ↓
ICMP Host Discovery
        ↓
TCP SYN Port Scanning
        ↓
Service Enumeration
        ↓
RDP Target Identification
        ↓
Hydra Brute Force Attack
        ↓
Traffic Capture in Wireshark
        ↓
SOC Investigation & Analysis
</pre>

<h2>⚔️ Attack Scenarios Simulated</h2>

<hr>

<h2>🎯 MITRE ATT&CK Mapping</h2>

<table>
<tr>
<th>Attack Activity</th>
<th>MITRE Technique</th>
<th>Technique ID</th>
</tr>

<tr>
<td>ICMP Reconnaissance</td>
<td>Network Service Discovery</td>
<td>T1046</td>
</tr>

<tr>
<td>TCP SYN Scan</td>
<td>Network Service Discovery</td>
<td>T1046</td>
</tr>

<tr>
<td>Service Enumeration</td>
<td>Active Scanning</td>
<td>T1595</td>
</tr>

<tr>
<td>RDP Brute Force Attack</td>
<td>Password Guessing</td>
<td>T1110.001</td>
</tr>

</table>

<h3>1. ICMP Reconnaissance</h3>

<ul>
  <li>Host discovery using ICMP Echo Requests</li>
  <li>Detection of ICMP traffic in Wireshark</li>
</ul>

<h3>2. TCP SYN Scan</h3>

<ul>
  <li>Nmap SYN scan against target machine</li>
  <li>Detection of SYN packets and scanning behavior</li>
</ul>

<h3>3. Service Enumeration</h3>

<ul>
  <li>Service version detection using Nmap</li>
  <li>Analysis of exposed services</li>
</ul>

<h3>4. RDP Brute Force Attack</h3>

<ul>
  <li>Hydra password attack simulation</li>
  <li>Detection of repeated authentication attempts</li>
</ul>

<hr>

<hr>

<h2>💻 Commands Used During Attack Simulation</h2>

<h3>ICMP Reconnaissance</h3>

<pre>
ping 192.168.74.130
</pre>

<h3>TCP SYN Scan</h3>

<pre>
nmap -sS 192.168.74.130
</pre>

<h3>Service Enumeration</h3>

<pre>
nmap -sV 192.168.74.130
</pre>

<h3>Hydra RDP Brute Force</h3>

<pre>
hydra -t 1 -V -f -l socuser -P passwords.txt rdp://192.168.74.130
</pre>

<hr>

<h2>🔍 Wireshark Filters Used</h2>

<h3>ICMP Traffic</h3>

<pre>
icmp
</pre>

<h3>TCP SYN Scan Detection</h3>

<pre>
tcp.flags.syn == 1 && tcp.flags.ack == 0
</pre>

<h3>RDP Traffic</h3>

<pre>
tcp.port == 3389
</pre>

<h3>HTTP Traffic</h3>

<pre>
http
</pre>

<h3>SMB Traffic</h3>

<pre>
tcp.port == 445
</pre>

<hr>

<h2>🛡️ SOC Investigation Findings</h2>

<ul>

<li>
Repeated ICMP Echo Requests indicated reconnaissance and host discovery activity.
</li>

<li>
Multiple TCP SYN packets targeting different ports suggested active port scanning behavior.
</li>

<li>
Service enumeration traffic exposed SMB, RDP, RPC, and HTTP-related services running on the target machine.
</li>

<li>
Hydra-generated authentication traffic demonstrated repeated login attempts consistent with brute force attack patterns.
</li>

<li>
Packet inspection revealed attacker behavior, communication patterns, and reconnaissance methodology used during early intrusion stages.
</li>

<li>
Wireshark packet analysis provided visibility into TCP flags, sequence numbers, destination ports, and protocol-level behavior.
</li>

</ul>

<h2>🧠 Skills Demonstrated</h2>

<ul>
  <li>Network Traffic Analysis</li>
  <li>Packet Inspection</li>
  <li>Threat Hunting</li>
  <li>Reconnaissance Detection</li>
  <li>SOC Investigation Workflow</li>
  <li>MITRE ATT&CK Mapping</li>
  <li>Attack Chain Analysis</li>
</ul>

<hr>

<h2>🖥️ Lab Environment</h2>

<table>
  <tr>
    <th>Machine</th>
    <th>Role</th>
  </tr>
  <tr>
    <td>Kali Linux</td>
    <td>Attacker</td>
  </tr>
  <tr>
    <td>Windows 10</td>
    <td>Victim</td>
  </tr>
</table>

<hr>

<h2>📄 Project Report</h2>

<p>
The complete detailed report is included in this repository.
</p>

<hr>

<h2>⚠️ Disclaimer</h2>

<p>
This project was performed inside an isolated virtual lab environment
for educational and defensive cybersecurity purposes only.
</p>
