# Vulnerability Assessment Report – OWASP Juice Shop

**Prepared by:** Pratik Giri  
**Date:** April 27, 2026  
**Classification:** CONFIDENTIAL

---

## Overview

This repository contains a professional Vulnerability Assessment Report for the intentionally vulnerable **OWASP Juice Shop** web application hosted at `juice-shop.herokuapp.com`.

The assessment was conducted using industry-standard tools and methodologies to identify security misconfigurations, missing headers, and potential attack vectors.

---

## Target Information

| Field | Details |
|---|---|
| Application | OWASP Juice Shop (Intentionally Vulnerable) |
| URL | https://juice-shop.herokuapp.com |
| IP Address | 54.220.192.176 (AWS eu-west-1) |
| Assessment Date | April 27, 2026 |
| Assessor | Pratik Giri (Kali Linux) |

---

## Tools Used

- **Nmap 7.95** – Network reconnaissance and port scanning
- **OWASP ZAP 2.17.0** – Passive web application vulnerability scanning
- **Browser DevTools** – Manual HTTP response header analysis

---

## Risk Summary

| Critical | High | Medium | Low | Informational |
|---|---|---|---|---|
| 0 | 0 | 4 | 4 | 2 |

---

## Key Findings

| # | Vulnerability | Risk | CWE |
|---|---|---|---|
| 1 | Content Security Policy (CSP) Header Not Set | Medium | CWE-693 |
| 2 | Cross-Domain Misconfiguration | Medium | CWE-264 |
| 3 | Missing Anti-clickjacking Header | Medium | CWE-1021 |
| 4 | Session ID in URL Rewrite | Medium | CWE-200 |
| 5 | Private IP Disclosure | Low | CWE-200 |
| 6 | Strict-Transport-Security Header Not Set | Low | CWE-319 |
| 7 | Timestamp Disclosure - Unix | Low | CWE-200 |
| 8 | X-Content-Type-Options Header Missing | Low | CWE-693 |
| 9 | Modern Web Application | Informational | N/A |
| 10 | Re-examine Cache-control Directives | Informational | CWE-524 |

---

## Files in This Repository

```
📄 Vulnerability_Assessment_Report_PratikGiri.docx   # Full report (Word format)
📄 README.md                                          # This file
```

---

## Methodology

The assessment followed a **black-box approach** across four phases:

1. **Network Reconnaissance** – Nmap service version scan to identify open ports and services
2. **Web Application Scanning** – OWASP ZAP 2.17.0 passive scan for security misconfigurations
3. **Manual Browser Analysis** – Chrome DevTools to inspect HTTP response headers in real time
4. **Reporting** – Aggregation, risk classification, and remediation recommendations

---

## Disclaimer

> This assessment was performed on **OWASP Juice Shop**, an intentionally vulnerable application designed for security training purposes. All findings are for educational use only. Do not perform security testing on applications without proper authorization.

---

*— Prepared by Pratik Giri | April 27, 2026 | Confidential —*
