# NETWORKWALKS-B082-WEEK2-PHASE1-2

 

🛡️ Penetration Testing Report 

Footprinting & Network Scanning Phases 

https://img.shields.io/badge/Cybersecurity-Ethical%20Hacking-blue https://img.shields.io/badge/Kali-Linux-purple https://img.shields.io/badge/Zenmap-Network%20Scanning-green https://img.shields.io/badge/Status-Completed-success 

👨‍💻 Author 

Mohammed Sadiq Bandiya 
Cybersecurity Professional | Ethical Hacking Enthusiast 

🔗 LinkedIn: https://www.linkedin.com/in/mohammed-sadiq-bandiya-80117017 

 

📌 Project Overview 

This repository contains my Week 2 Cybersecurity Internship Project completed as part of the Networkwalks Cybersecurity Program (Batch B082). 

The project focuses on two critical phases of a penetration testing engagement: 

Reconnaissance & Footprinting 

Network Scanning & Discovery 

The objective was to learn how security professionals and attackers gather publicly available information about a target organization and discover live systems within a network before performing deeper security assessments. 

 

⚠️ Disclaimer 

All activities documented in this repository were performed only on systems: 

Owned by me, or Explicitly authorized for testing through written permission. 

This project is strictly for educational, training, and research purposes. Unauthorized scanning, probing, or access to systems you do not own or have permission to test may violate laws and regulations. 

 

🎯 Objectives 

The objectives of this project were to: 

Perform passive and active reconnaissance. 

Gather public information about a target domain. 

Enumerate DNS records and web technologies. 

Identify exposed infrastructure details. 

Discover active hosts on a local network. 

Create network topology documentation. 

Analyze findings and assess potential security risks. 

Produce professional penetration testing documentation. 

 

🛠️ Tools Used 

Tool 

Purpose 

Kali Linux 

Operating system for reconnaissance activities 

WHOIS 

Domain registration information gathering 

WhatWeb 

Website technology fingerprinting 

Nslookup 

DNS resolution and IP discovery 

Curl 

HTTP header analysis 

Wafw00f 

Web Application Firewall detection 

DNSRecon 

DNS enumeration 

GHDB (Google Hacking Database) 

Google Dork reconnaissance 

Zenmap (Nmap GUI) 

Network discovery and host scanning 

Windows Command Prompt 

Network configuration verification 

 

📚 Modules Completed 

W2-PM1 

Footprinting & Reconnaissance Attacks with Multiple Kali Tools 

W2-PM2 

Footprinting & Reconnaissance Attacks with GHDB 

W2-PM5 

Network Scanning with Zenmap 

 

🔍 Phase 1: Reconnaissance & Footprinting 

The reconnaissance phase focused on collecting publicly available information regarding the target domain. 

Activities Performed 

WHOIS Enumeration 

Used WHOIS to gather: 

Domain registration information 

Registrar details 

Domain creation and expiration dates 

Name server information 

Purpose: Understanding domain ownership and infrastructure configuration. 

 

WhatWeb Fingerprinting 

Used WhatWeb to identify: 

Web server technologies 

CMS platforms 

Plugins 

Cookies 

Web framework information 

Findings 

Apache Web Server 

WordPress CMS 

WordPress Download Manager Plugin 

Additional web technology fingerprints 

Purpose: Technology fingerprinting helps identify technologies requiring further security review. 

 

DNS Resolution with Nslookup 

Resolved the target domain and obtained its IP address. 

Purpose: Mapping domains to infrastructure resources. 

 

HTTP Header Analysis with Curl 

Inspected HTTP response headers using: 

1     curl -I https://target-domain.com 

Information obtained included: 

Server responses 

Security headers 

API exposure indicators 

Application response behavior 

 

WAF Detection using Wafw00f 

Identified: 

Web Application Firewall presence 

Protection technologies 

Finding 

ModSecurity (SpiderLabs) 

Purpose: Understanding defensive controls protecting web applications. 

 

DNS Enumeration using DNSRecon 

Enumerated: 

A Records 

MX Records 

NS Records 

TXT Records 

SPF Records 

SRV Records 

Purpose: Building an infrastructure profile of the target environment. 

 

Google Hacking Database (GHDB) 

Used Google Dorks to identify publicly indexed information. 

The exercise demonstrated how search engines may expose: 

Login portals 

Open directories 

Documents 

Configuration files 

Internet-facing assets 

 

🌐 Phase 2: Network Scanning 

Network scanning was performed against an authorized local network using Zenmap. 

 

Network Discovery 

The following steps were carried out: 

1. Identify Local Network Configuration 

Using: 

1     ipconfig 

Information gathered: 

Local IP address 

Default Gateway 

Subnet Information 

 

2. Host Discovery with Zenmap 

Performed: 

Ping Scan 

Live Host Discovery 

MAC Address Enumeration 

Discovered: 

Active hosts on the subnet 

Device information 

Network accessibility 

 

3. Network Topology Mapping 

Generated: 

Network topology visualization 

Device relationship mapping 

Infrastructure overview 

 

📊 Key Findings 

Finding 

Description 

Technology Exposure 

Web technologies and plugin versions were publicly visible 

IP Disclosure 

Domain successfully resolved to a public IP address 

HTTP Information Exposure 

Server headers disclosed technical details 

WAF Detection 

ModSecurity identified protecting the web application 

DNS Exposure 

DNS records revealed infrastructure information 

Live Hosts Detected 

Multiple active hosts discovered in the local environment 

 

⚠️ Risk Analysis 

Risk 

Potential Impact 

Technology Fingerprinting 

Facilitates targeted attacks 

Infrastructure Disclosure 

Reveals network architecture 

DNS Enumeration 

Provides reconnaissance intelligence 

Header Exposure 

Assists attacker profiling efforts 

Network Device Visibility 

Identifies active systems for further assessment 

Public Information Exposure 

Expands attack surface awareness 

Important: These observations are informational findings and do not represent confirmed vulnerabilities. Further authorized testing would be required to determine exploitability. 

 

✅ Recommendations 

Web Security 

Minimize technology exposure. 

Regularly update CMS platforms and plugins. 

Review publicly accessible application metadata. 

Reduce unnecessary HTTP header disclosures. 

DNS Security 

Review DNS records periodically. 

Remove obsolete entries. 

Monitor publicly exposed services. 

Network Security 

Conduct regular internal network scans. 

Maintain accurate asset inventories. 

Investigate unknown devices promptly. 

Update network diagrams regularly. 

Security Operations 

Continuously monitor WAF effectiveness. 

Perform periodic vulnerability assessments. 

Ensure testing activities remain within authorized scope. 

 

🎓 Learning Outcomes 

Throughout this project I gained practical experience in: 

Reconnaissance methodology 

Open-source intelligence gathering (OSINT) 

Domain and DNS enumeration 

Web application fingerprinting 

Infrastructure discovery 

Network scanning and host enumeration 

Risk assessment 

Professional cybersecurity reporting 

This exercise highlighted the importance of information gathering as a foundational phase of penetration testing and demonstrated how publicly available information can contribute significantly to understanding an organization's attack surface. 

 

📂 Repository Structure 

1     . 

2     ├── README.md 

3     ├── Report/ 

4     │   └── W2-PM-FINAL-Report.pdf 

5     ├── Screenshots/ 

6     │   ├── whois.png 

7     │   ├── whatweb.png 

8     │   ├── nslookup.png 

9     │   ├── curl.png 

10     │   ├── wafw00f.png 

11     │   ├── dnsrecon.png 

12     │   └── zenmap.png 

13     └── Evidence/ 

 

🏆 Program Information 

Item 

Value 

Program 

Networkwalks Cybersecurity Program 

Batch 

B082 

Week 

02 

Project Type 

Penetration Testing 

Focus Area 

Footprinting & Network Scanning 

 

📜 Conclusion 

This project successfully demonstrated the practical application of penetration testing methodologies during the reconnaissance and scanning phases. Through the use of industry-standard tools such as WHOIS, WhatWeb, DNSRecon, Wafw00f, and Zenmap, valuable insights were obtained regarding target infrastructure, publicly available information, and network visibility. 

The experience reinforced the importance of conducting ethical, authorized security assessments and maintaining clear, professional documentation throughout the testing lifecycle. 
