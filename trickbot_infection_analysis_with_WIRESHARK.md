# Trickbot Malware Analysis

This repository contains a comprehensive analysis of a Trickbot malware infection observed on a Windows 7 machine. The analysis includes network traffic examination, identification of malicious payloads, and extraction of sensitive information.

## 🧪 Infection Overview

- **Infected Host:** `CAT-BOMB-W7-PC`
- **Malware:** Trickbot
- **Observation Date:** May 28, 2020

## 📡 Network Traffic Analysis

Captured HTTP POST requests revealed data exfiltration activities:

- **Endpoint:** `http://203.176.135.102:8082/yas33/`
- **Data Exfiltrated:**
  - System process list
  - Network configuration (`ipconfig /all`)
  - Domain and user information

## 🧾 Extracted Information

- **User Accounts:**
  - `phillip.ghent`
  - `timothy.sizemore`
- **Hostnames:**
  - `CAT-BOMB-W7-PC`
  - `CAT-BOMB-W10-PC`
- **Domain Controller:** `Catbomber-DC.catbomber.net`

## 🐟 Malicious Payloads

Two executable files were identified being downloaded under the guise of image files:

1. **Filename:** `imgpaper.png`
   - **SHA256:** `a1b2c3d4e5f67890123456789abcdef1234567890abcdef1234567890abcdef1`
2. **Filename:** `imgicon.png`
   - **SHA256:** `1f2e3d4c5b6a7980123456789abcdef1234567890abcdef1234567890abcdef2`

*Note: Actual hashes should be computed from the extracted files.*

## 🔐 Credential Extraction

Trickbot's password-grabbing module (`pwgrab32`) was observed exfiltrating credentials, including email passwords and browser-stored logins.

## 📁 Repository Contents

- `pcap/`: Captured network traffic files
- `extracted/`: Extracted malicious payloads
- `analysis/`: Detailed analysis reports and scripts

## 🛡️ Disclaimer

This repository is for educational and research purposes only. Handling malware samples poses risks; ensure proper precautions are taken.
## 📁 Data Source

The analysis in this repository is based on the Trickbot infection sample from Malware Traffic Analysis:

🔗 [Malware Traffic Analysis – May 28, 2020 Sample](https://malware-traffic-analysis.net/2020/05/28/index.html)

This resource provided the packet capture (pcap) files and contextual information used for the analysis.
