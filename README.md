# OSINT & Digital Footprinting: Infrastructure Analysis of Apart.pl

## Project Overview
This project was developed as part of the **Network Exploration** (*Eksploracja Sieci Teleinformatycznych*) course at the **Military University of Technology**. The goal was to conduct a comprehensive passive reconnaissance of `apart.pl`, identifying its digital footprint, business intelligence, and human-related attack surfaces without any direct interaction with the target's systems.

## Key Areas of Investigation
The investigation utilized advanced OSINT methodologies to map the target across multiple layers:

* **Business & Financial Intelligence:**
    * Analysis of legal status, financial results (2021-2024), and corporate connections via `Aleo`, `KRS`, and `OWG`.
    * Identification of corporate bank accounts and verifying provider identifiers.
* **Technical Infrastructure & Topology:**
    * DNS infrastructure mapping including `DNSSEC` validation and server geolocation.
    * Deep-dive host analysis using `Censys.io` and `Shodan.io` to identify services like `MFT Serv-U` or `enova365`.
    * Website traffic analysis and historical sitemap evolution via `SimilarWeb` and `Wayback Machine`.
* **Human OSINT & Data Breaches:**
    * Identification of key employees and organizational structure through `LinkedIn`, `Hunter.io`, and `Tomba.io`.
    * Social media footprinting to map personal interests and potential physical locations.
    * Cross-referencing corporate emails with historical data breaches via `HaveIBeenPwned`.
* **Security Posture & Mobile Analysis:**
    * Evaluation of HTTP security headers and `DMARC` records.
    * Analysis of the mobile application for trackers and excessive permissions using `Exodus Privacy`.
    * Metadata extraction from public PDF documents to identify internal software versions (Adobe InDesign).

## Tools Used
* **Technical Recon:** `Shodan.io`, `Censys.io`, `DNSdumpster`, `Wappalyzer`, `BuiltWith`.
* **Business/Legal:** `KRS`, `Aleo.com`, `dns.pl/whois`.
* **Human/Breach:** `LinkedIn`, `Hunter.io`, `Tomba.io`, `HaveIBeenPwned`, `WhatsMyName`.
* **Mobile & Forensics:** `Exodus Privacy`, `Metadata2Go`.
* **General OSINT:** `Google Dorks`, `Wayback Machine`, `SimilarWeb`.

---
## Deep Dive: Vulnerability or Honeypot?

The most intriguing discovery during the reconnaissance was a **SolarWinds Serv-U (v15.2.5)** server identified on host `91.209.27.12`.

## Critical Vulnerabilities
This specific version is outdated and remains vulnerable to several critical flaws patched in newer releases (15.4.x):
* **CVE-2024-28995:** A critical path traversal vulnerability allowing an unauthenticated attacker to read arbitrary files from the server (e.g., sensitive config files).
* **CVE-2024-0371 & CVE-2023-35718:** Additional flaws that could lead to unauthorized data access.

## The "Honeypot" Hypothesis
The presence of such a glaringly vulnerable system in a professional infrastructure led to a fascinating conclusion: **this might be a Honeypot.** 

A Honeypot is a decoy system designed to lure, identify, and analyze attackers. If this is the case:
* **Detection:** Any interaction beyond a simple port scan is immediately logged for threat intelligence.
* **Analysis:** Attackers' IP addresses and methods are recorded to strengthen the company's real production systems.
* **Deception:** Any files available for download are likely fake data meant to confirm successful exploitation and track attacker intent.

**Conclusion:** Identifying this host highlights the importance of distinguishing between a neglected server and a deliberate security measure.

## Full Report
The complete technical report (131 pages) contains detailed methodology, screenshots, and security conclusions.
[Download Project Report (PDF)](./Passive_Reconnaissance_APART_Report.pdf)
