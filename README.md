# Networkwalks-B084-Week-02-practical
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
