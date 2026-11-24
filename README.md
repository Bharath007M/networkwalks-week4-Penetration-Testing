# 🔐 WEEK 4 – PENETRATION TESTING & VULNERABILITY ASSESSMENT

## Mediroza General Hospital | NETWORKWALKS

A hands-on black-box web application security assessment completed as part of the **NETWORKWALKS Week 4 Capstone Project – Batch B084**.

The assessment focused on reconnaissance, patient portal security, PDF password protection, potential SQL injection, and sensitive database exposure.

---

## 🎯 Project Overview

| Detail | Information |
|---|---|
| Project | Mediroza General Hospital |
| Organization | NETWORKWALKS |
| Batch | B084 |
| Week | Week 4 |
| Assessment Type | Black-box Penetration Testing |
| Target | `https://medirozahospital.com` |
| Duration | Five days |
| Status | Assessment Completed |

> **Note:** This repository documents an authorized educational exercise. Testing was limited to the agreed target and scope.

---

## 📌 Project Objectives

- Perform reconnaissance and identify exposed web services.
- Examine patient portal authentication and access controls.
- Assess encrypted patient PDF reports and password strength.
- Review potential SQL-related data exposure.
- Document findings, evidence, risk ratings, and remediation recommendations.

---

## 🛠️ Tools Used

- **Nmap** – Network scanning and service discovery
- **Gobuster** – Web directory and content discovery
- **Nslookup** – DNS information gathering
- **cURL** – HTTP request and response inspection
- **PDF Hash Extraction Tool** – Encrypted PDF hash extraction
- **Password Cracking Tool** – PDF password security testing
- **Web Browser** – Portal and application assessment

---

## 📂 Project Milestones

### M1 – Reconnaissance and Initial Assessment

- Performed DNS and HTTP information gathering.
- Reviewed `robots.txt` for publicly listed paths.
- Used Nmap to identify open web ports.
- Used Gobuster for content discovery.

**Observation:** Ports 80 and 443 were shown as open in the supplied scan evidence. Directory discovery also returned several restricted responses.

### M2 – PDF Password Security Testing

- Identified three encrypted patient report entries in the portal.
- Extracted a crackable hash from an encrypted PDF.
- Observed successful password-cracking results.

**Observation:** The supplied screenshots support hash extraction and two successful cracking states. Complete password-to-file mapping requires further verification.

### M3 – Staff and Shareholder Data Exposure

- Identified the database backup file `mediroza_db_backup_2019.sql`.
- Examined the backup for staff-related and shareholder information.
- Documented the potential exposure of employee contact details, salary information, and shareholder details.

**Preliminary Risk:** High

**Note:** The report distinguishes the database-backup observation from independently validated access through the suspected SQL-related route. Sensitive records are not reproduced in this repository.

### M4 – Final Penetration Testing Report

Prepared the final report with:

- Executive Summary
- Scope and Methodology
- Findings and Proof of Exploitation
- Risk Rating
- Recommendations and Remediation
- Evidence Register
- Safe Evidence Handling Guidelines

---

## ⚠️ Key Security Observations

| Finding | Observation | Preliminary Rating |
|---|---|---|
| F-01 | Information disclosure through `robots.txt` paths | Low |
| F-02 | Suspected SQL injection or authentication bypass | High – Provisional |
| F-03 | Patient report listing and access-control concerns | High – Provisional |
| F-04 | Weak PDF password protection | High – Provisional |
| M3 | Staff and shareholder database exposure assessment | Requires final validation |

Risk ratings are preliminary and should be updated after confirming exploitability, access conditions, and impact.

---

## 🛡️ Recommendations and Remediation

- Use parameterized SQL queries to prevent SQL injection.
- Implement server-side authentication and authorization.
- Restrict access to patient reports and sensitive files.
- Store database backups outside publicly accessible directories.
- Encrypt database backups and apply strict access controls.
- Use strong, unique passwords for encrypted documents.
- Avoid relying on `robots.txt` to protect sensitive resources.
- Monitor application logs for suspicious authentication activity.

---

## 📸 Evidence and Documentation

The repository contains supporting project evidence and the final report.

```text
Week-4-Penetration-Testing/
│
├── README.md
│
├── screenshots/
│   ├── Reconnaissance/
│   ├── Nmap-Gobuster/
│   ├── Patient-Portal/
│   ├── PDF-Hash-Extraction/
│   └── Password-Testing/
│
└── Mediroza_General_Hospital_Pentest_Report_With_Evidence.pdf
```

*Folder names above are an example structure; adjust them to match the actual repository.*

---

## 📑 Final Report

The complete penetration testing report includes the assessment scope, methodology, findings, risk ratings, remediation guidance, and redacted evidence.

**Report:** `Mediroza_General_Hospital_Pentest_Report_With_Evidence.pdf`

---

## 💡 Key Learning Outcomes

- Understanding the penetration testing methodology.
- Performing reconnaissance and web content discovery.
- Assessing authentication and access-control weaknesses.
- Understanding PDF encryption and password security.
- Identifying risks associated with exposed database backups.
- Preparing professional security reports and documenting evidence safely.

---

## 🙏 Acknowledgement

Special thanks to **NETWORKWALKS** and **Sir Waqas Karim (CCIE)** for their guidance, support, and learning opportunities throughout this cybersecurity training journey.

---

## ⚠️ Disclaimer

This repository is intended for educational and authorized security assessment purposes only. Do not use the techniques described here against systems without explicit permission.

Sensitive patient, employee, shareholder, password, and authentication information must not be published.

---

**#CyberSecurity #PenetrationTesting #EthicalHacking #NETWORKWALKS #WebSecurity #InfoSec**
