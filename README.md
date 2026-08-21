# Penetration Testing Report: Footprinting & Network Scanning

🛡️ **Week 2 Cybersecurity Internship Project** | NetworkWalks Batch B082

---

## Table of Contents

- [About](#about)
- [Project Overview](#project-overview)
- [Disclaimer](#disclaimer)
- [Objectives](#objectives)
- [Tools & Technologies](#tools--technologies)
- [Phases](#phases)
  - [Phase 1: Reconnaissance & Footprinting](#phase-1-reconnaissance--footprinting)
  - [Phase 2: Network Scanning](#phase-2-network-scanning)
- [Key Findings](#key-findings)
- [Risk Analysis](#risk-analysis)
- [Recommendations](#recommendations)
- [Learning Outcomes](#learning-outcomes)
- [Repository Structure](#repository-structure)
- [Conclusion](#conclusion)

---

## About

**Author:** Mohammed Sadiq Bandiya  
**Role:** Cybersecurity Professional | Ethical Hacking Enthusiast  
**LinkedIn:** https://www.linkedin.com/in/mohammed-sadiq-bandiya-80117017

---

## Project Overview

This repository documents my Week 2 Cybersecurity Internship Project completed as part of the NetworkWalks Cybersecurity Program (Batch B082).

The project focuses on two critical phases of a penetration testing engagement:

1. **Reconnaissance & Footprinting** - Gathering publicly available information about target organizations
2. **Network Scanning & Discovery** - Identifying live systems within authorized networks

The objective was to learn how security professionals and ethical hackers perform reconnaissance and discover network infrastructure before conducting deeper security assessments.

---

## Disclaimer

⚠️ **Important:** All activities documented in this repository were performed only on systems that I:

- Own, or
- Have explicit written permission to test

This project is strictly for **educational, training, and research purposes only**. Unauthorized scanning, probing, or access to systems you do not own or have permission to test may violate applicable laws and regulations.

---

## Objectives

The primary objectives of this project were to:

- ✅ Perform passive and active reconnaissance
- ✅ Gather public information about target domains
- ✅ Enumerate DNS records and web technologies
- ✅ Identify exposed infrastructure details
- ✅ Discover active hosts on local networks
- ✅ Create network topology documentation
- ✅ Analyze findings and assess potential security risks
- ✅ Produce professional penetration testing documentation

---

## Tools & Technologies

| Tool | Purpose |
|------|---------|
| **Kali Linux** | Operating system for reconnaissance activities |
| **WHOIS** | Domain registration information gathering |
| **WhatWeb** | Website technology fingerprinting |
| **Nslookup** | DNS resolution and IP discovery |
| **Curl** | HTTP header analysis |
| **Wafw00f** | Web Application Firewall detection |
| **DNSRecon** | DNS enumeration and record discovery |
| **GHDB** | Google Hacking Database for reconnaissance |
| **Zenmap** | Network discovery and host scanning (Nmap GUI) |
| **Windows Command Prompt** | Network configuration verification |

### Modules Completed

- **W2-PM1** - Footprinting & Reconnaissance Attacks with Multiple Kali Tools
- **W2-PM2** - Footprinting & Reconnaissance Attacks with GHDB
- **W2-PM5** - Network Scanning with Zenmap

---

## Phases

### Phase 1: Reconnaissance & Footprinting

The reconnaissance phase focused on collecting publicly available information regarding the target domain.

#### 1.1 WHOIS Enumeration

**Tools Used:** WHOIS  
**Information Gathered:**
- Domain registration information
- Registrar details
- Domain creation and expiration dates
- Name server information

**Purpose:** Understanding domain ownership and infrastructure configuration.

---

#### 1.2 WhatWeb Fingerprinting

**Tools Used:** WhatWeb  
**Technologies Identified:**
- Web server technologies
- CMS platforms and versions
- Installed plugins
- Cookies and tracking
- Web framework information

**Findings:**
- Apache Web Server
- WordPress CMS
- WordPress Download Manager Plugin
- Additional web technology fingerprints

**Purpose:** Technology fingerprinting helps identify technologies requiring further security review.

---

#### 1.3 DNS Resolution with Nslookup

**Tools Used:** Nslookup  
**Activities:**
- Resolved target domain
- Obtained associated IP addresses

**Purpose:** Mapping domains to infrastructure resources.

---

#### 1.4 HTTP Header Analysis with Curl

**Tools Used:** Curl  
**Command:** `curl -I https://target-domain.com`

**Information Obtained:**
- Server response details
- Security headers
- API exposure indicators
- Application behavior characteristics

**Purpose:** Understanding server configuration and potential information disclosure.

---

#### 1.5 WAF Detection using Wafw00f

**Tools Used:** Wafw00f  
**Identified:**
- Web Application Firewall presence
- Protection technologies deployed

**Finding:** ModSecurity (SpiderLabs) detected

**Purpose:** Understanding defensive controls protecting web applications.

---

#### 1.6 DNS Enumeration using DNSRecon

**Tools Used:** DNSRecon  
**Records Enumerated:**
- A Records
- MX Records
- NS Records
- TXT Records
- SPF Records
- SRV Records

**Purpose:** Building a comprehensive infrastructure profile of the target environment.

---

#### 1.7 Google Hacking Database (GHDB)

**Tools Used:** Google Dorks  
**Information Demonstrated:**
- Login portals publicly indexed
- Open directories
- Documents and archives
- Configuration files
- Internet-facing assets

**Purpose:** Understanding how search engines may expose sensitive organizational information.

---

### Phase 2: Network Scanning

Network scanning was performed against an authorized local network using Zenmap.

#### 2.1 Network Discovery

**Step 1: Identify Local Network Configuration**

Command: `ipconfig`

Information Gathered:
- Local IP address
- Default gateway
- Subnet information

**Step 2: Host Discovery with Zenmap**

Activities Performed:
- Ping Scan
- Live Host Discovery
- MAC Address Enumeration

Discovered:
- Active hosts on the subnet
- Device information
- Network accessibility status

**Step 3: Network Topology Mapping**

Generated Outputs:
- Network topology visualization
- Device relationship mapping
- Infrastructure overview

---

## Key Findings

| Finding | Description | Implication |
|---------|-------------|-------------|
| **Technology Exposure** | Web technologies and plugin versions publicly visible | Enables targeted attack research |
| **IP Disclosure** | Domain successfully resolved to public IP | Reveals hosting infrastructure |
| **HTTP Information Exposure** | Server headers disclose technical details | Facilitates reconnaissance |
| **WAF Detection** | ModSecurity identified as protection layer | Documents defensive controls |
| **DNS Exposure** | DNS records reveal infrastructure information | Maps network architecture |
| **Live Hosts Detected** | Multiple active hosts in local environment | Identifies assessment targets |

---

## Risk Analysis

| Risk | Potential Impact | Severity |
|------|-----------------|----------|
| **Technology Fingerprinting** | Facilitates targeted attacks based on known vulnerabilities | Medium-High |
| **Infrastructure Disclosure** | Reveals network architecture and relationships | Medium |
| **DNS Enumeration** | Provides reconnaissance intelligence for attackers | Medium |
| **Header Exposure** | Assists attacker profiling and reconnaissance efforts | Low-Medium |
| **Network Device Visibility** | Identifies active systems for further assessment | Medium |
| **Public Information Exposure** | Expands overall attack surface awareness | Medium |

**⚠️ Important Note:** These observations are informational findings and do not represent confirmed vulnerabilities. Further authorized testing would be required to determine actual exploitability and prioritize remediation efforts.

---

## Recommendations

### Web Security

- Minimize unnecessary technology disclosure in HTTP headers
- Regularly update CMS platforms and plugins
- Review publicly accessible application metadata
- Implement security headers to limit information exposure
- Monitor for outdated or vulnerable components

### DNS Security

- Periodically review DNS records for accuracy and necessity
- Remove obsolete or unused DNS entries
- Monitor publicly exposed services and subdomains
- Implement DNSSEC where applicable
- Restrict DNS zone transfers

### Network Security

- Conduct regular internal network scans and audits
- Maintain accurate and up-to-date asset inventories
- Investigate and document unknown devices promptly
- Update network diagrams regularly
- Implement network segmentation

### Security Operations

- Continuously monitor WAF effectiveness and logs
- Perform periodic vulnerability assessments
- Maintain a regular penetration testing schedule
- Ensure all testing activities remain within authorized scope
- Document all security testing activities

---

## Learning Outcomes

Through this project, I gained practical experience in:

- ✓ Reconnaissance methodology and best practices
- ✓ Open-source intelligence gathering (OSINT)
- ✓ Domain and DNS enumeration techniques
- ✓ Web application fingerprinting
- ✓ Infrastructure and network discovery
- ✓ Network scanning and host enumeration
- ✓ Risk assessment and analysis
- ✓ Professional cybersecurity reporting

This exercise highlighted the importance of information gathering as a foundational phase of penetration testing and demonstrated how publicly available information can significantly contribute to overall security risk.

---

## Repository Structure

```
.
├── README.md                          # Project documentation
├── Report/
│   └── W2-PM-FINAL-Report.pdf        # Comprehensive penetration testing report
├── Screenshots/
│   ├── whois.png                      # WHOIS enumeration results
│   ├── whatweb.png                    # Web technology fingerprinting
│   ├── nslookup.png                   # DNS resolution results
│   ├── curl.png                       # HTTP header analysis
│   ├── wafw00f.png                    # WAF detection results
│   ├── dnsrecon.png                   # DNS enumeration results
│   └── zenmap.png                     # Network scanning results
└── Evidence/                          # Supporting documentation and evidence
```

---

## Conclusion

This project successfully demonstrated the practical application of penetration testing methodologies during the reconnaissance and scanning phases. Through the use of industry-standard tools such as WHOIS, DNSRecon, Zenmap, and others, I developed a comprehensive understanding of how to conduct systematic reconnaissance and network discovery.

The experience reinforced the critical importance of:

- Conducting **ethical and authorized** security assessments
- Maintaining **clear, professional documentation** throughout the testing lifecycle
- Understanding the **complete scope and authorization** before initiating any testing activities
- Properly analyzing findings and providing **actionable recommendations**

This foundational knowledge serves as a stepping stone for more advanced penetration testing phases and demonstrates the practical application of cybersecurity principles in real-world scenarios.

---

**License:** Educational Use Only  
**Last Updated:** August 2026  
**Status:** Complete

