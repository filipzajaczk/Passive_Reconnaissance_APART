# OSINT & Digital Footprinting: Infrastructure Analysis of Apart.pl

## Project Overview
This project was developed as part of the **Network Exploration** (*Eksploracja Sieci Teleinformatycznych*) course at the **Military University of Technology**. The goal was to conduct a comprehensive passive reconnaissance of `apart.pl`, identifying its digital footprint, business intelligence, and human-related attack surfaces without any direct interaction with the target's systems.

## Key Areas of Investigation
The investigation utilized advanced OSINT methodologies to map the target across multiple layers:

* **Business & Financial Intelligence:** * Analysis of legal status, financial results (2021-2024), and corporate connections via `Aleo`, `KRS`, and `OWG`.
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

## Full Report
The complete technical report (131 pages) contains detailed methodology, screenshots, and security conclusions.
[Download Project Report (PDF)](./Passive_Reconnaissance_APART_Report.pdf)
