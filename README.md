# Networkwalks-B084-Week-02-practical


# Module 1: Foot printing and Reconnaissance

This folder contains my practical work for Week 2, PM1.

## Tools Used
- WHOIS
- WhatWeb
- Nslookup
- cURL
- WAFW00F
- DNSRecon

## Evidence
Screenshots and saved command outputs for each practical task.

-------------------------------------------------------------------------------------------------------------------------------------------------------------------

# Module 2: Footprinting & Reconnaissance with GHDB

## Overview
This module focuses on passive reconnaissance using the Google Hacking Database (GHDB) hosted on Exploit-DB. By using specialized search operators (Google Dorks), sensitive information and publicly exposed assets are identified without directly interacting with target systems.

---

## Tasks Completed

### Task 1: Exposed Security Cameras
Found live, publicly accessible security camera feeds using GHDB dorks.

| No. | Link | Relevant Dork | Username / Password |
|---|---|---|---|
| 1 | http://122.116.41.8:8080/ | `intitle:"webcamXP" inurl:8080` | N/A |

---

### Task 2: Mathematics eBooks (PDF)
Found downloadable mathematics textbooks in PDF format using index listing dorks.

| No. | Link | Relevant Dork | Username / Password |
|---|---|---|---|
| 1 | https://www.skylineuniversity.ac.ae/pdf/math/ | `intitle:index.of "parent directory" mathematics pdf` | N/A |

---

## Key Takeaways
Google Dorks demonstrate how search engine crawlers index misconfigured web servers. Security teams use these same queries to conduct self-audits and remediate unintended exposure.

-------------------------------------------------------------------------------------------------------------------------------------------------------------------

# Module 3: Footprinting with Maltego

## Overview
This module demonstrates visual link analysis and data integration using Maltego to harvest infrastructure and contact details for a target domain.

---

## Objectives & Tasks
1. **Installation & Setup:** Configured Maltego Community Edition (CE) and authenticated a free Maltego account.
2. **Entity Execution:** Added a target Domain entity (`networkwalks.com`) and executed email harvesting transforms to collect related organizational contact addresses.

---

## Findings & Deliverables
* **Target Domain:** `networkwalks.com`
* **Transform Run:** `To Email addresses [From Domain]`
* **Privacy Mode:** Normal

---

## Key Takeaways
Maltego synthesizes disparate OSINT endpoints into structured graphical representations, streamlining the identification of organizational relationships, email structures, and potential targets for social engineering assessments.

-------------------------------------------------------------------------------------------------------------------------------------------------------------------

# Module 4: Footprinting & Reconnaissance with theHarvester

## Overview
This module utilizes `theHarvester`, a Python-based OSINT tool, to gather emails, subdomains, hostnames, and open ports across multiple public search engines and database APIs.

---

## Tasks & Executed Commands

### Task 1: Search via Baidu Source
Querying target domain `microsoft.com` using the Baidu engine with a result limit of 1000.
```bash
theHarvester -d microsoft.com -l 1000 -b baidu

-------------------------------------------------------------------------------------------------------------------------------------------------------------------

# Module 5: Network Scanning with Zenmap

## Overview

This module focuses on active local network scanning, host discovery, and network topology mapping using **Zenmap** (the official graphical user interface for Nmap). The primary objective of this exercise is to identify live assets across a designated IP range, document active hardware MAC addresses, and establish a baseline for internal network auditing.

## Lab Setup & Execution

* **Target Subnet:** `10.0.0.0/24`
* **Scan Profile Used:** `Ping Scan`
* **Tooling:** Zenmap / Nmap

## Host Discovery Summary

A **Ping Scan** was executed across the `10.0.0.0/24` subnet. A total of **4 active hosts** were identified on the local network segment.

### Active Hosts Table

| IP Address | MAC Address | Device / Interface | Status |
| --- | --- | --- | --- |
| `10.0.0.1` | `00:50:56:E3:B3:2C` | Active Host | Up |
| `10.0.0.4` | `00:0C:29:C0:94:8F` | Active Host | Up |
| `10.0.0.19` | `00:50:56:E9:64:82` | Active Host | Up |
| `10.0.0.50` | `00:0C:29:40:C0:93` | Local Workstation | Up |

## Key Takeaways & Security Insights

1. **Asset Discovery & Baseline:** Ping scanning provides a fast and efficient method for security analysts to enumerate live systems on an IP subnet without generating heavy port-scanning noise.
2. **Hardware Auditing:** Capturing hardware MAC addresses along with IP bindings helps trace network interface vendors (e.g., VMware OUI prefixes like `00:50:56` and `00:0C:29`) and detect unauthorized hardware or rogue devices connected to the internal network.
3. **Internal Security Monitoring:** Regular host discovery scans form the foundation for attack surface management, asset inventory tracking, and vulnerability management workflows.

-------------------------------------------------------------------------------------------------------------------------------------------------------------------
