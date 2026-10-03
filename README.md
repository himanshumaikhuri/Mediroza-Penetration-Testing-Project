<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:0b1026,45:1f6feb,100:7c3aed&height=185&section=header&text=Mediroza%20Security%20Assessment&fontSize=38&fontColor=ffffff&animation=fadeIn&fontAlignY=35&desc=Networkwalks%20B082%20%7C%20Week%204%20Capstone%20Project&descAlignY=55&descSize=17" alt="Mediroza Security Assessment">

<p align="center">
  <strong>Black Box Web Application Penetration Test</strong><br>
  <sub>Authorized educational security assessment</sub>
</p>

<p align="center">
  <img alt="Assessment type: Black box" src="https://img.shields.io/badge/ASSESSMENT-BLACK%20BOX-1f6feb?style=for-the-badge&labelColor=0b1026">
  <img alt="Overall risk: Critical" src="https://img.shields.io/badge/OVERALL%20RISK-CRITICAL-dc2626?style=for-the-badge&labelColor=0b1026">
</p>
<p align="center">
  <img alt="Seven findings" src="https://img.shields.io/badge/FINDINGS-7-f59e0b?style=flat-square&labelColor=111827">
  <img alt="Three critical findings" src="https://img.shields.io/badge/CRITICAL-3-dc2626?style=flat-square&labelColor=111827">
  <img alt="Two high findings" src="https://img.shields.io/badge/HIGH-2-f97316?style=flat-square&labelColor=111827">
  <img alt="Authorized testing" src="https://img.shields.io/badge/STATUS-AUTHORIZED-16a34a?style=flat-square&labelColor=111827">
</p>

**Overall risk rating: CRITICAL.** This controlled assessment identified an attack path from a public-facing login page to confidential patient documents, staff financial records, and corporate ownership information.

---

## 📌 Project Overview

This repository documents a black-box penetration test of the Mediroza General Hospital web infrastructure at `https://medirozahospital.com`. The assessment was performed for the Networkwalks B082 Week 4 Capstone Project to identify weaknesses, demonstrate their impact through controlled exploitation, and recommend practical remediation.

Seven findings, ranging from **Medium** to **Critical**, were identified. The central issue was a SQL injection vulnerability in the patient portal login flow. In the authorized test environment, it enabled authentication bypass, access to confidential patient lab-report PDFs, discovery of sensitive PDF metadata, and retrieval of an exposed database backup containing staff salary and shareholder information.

---

## 🎯 Objectives

- Assess the web application from an external, unauthenticated perspective.
- Identify weaknesses in authentication, input handling, file protection, and server configuration.
- Demonstrate the real-world impact of each finding in a controlled manner.
- Document evidence and provide prioritized remediation recommendations.

---

## 🔒 Authorization and Scope

Testing was conducted with written authorization from the client as part of a controlled Networkwalks educational exercise.

| In Scope | Excluded from Scope |
| --- | --- |
| `https://medirozahospital.com` | Social engineering |
| Public-facing web application behavior | Denial of service testing |
| Patient portal and discovered web paths within domain | Any testing outside the agreed domain |

---

## 🛠️ Methodology & Assessment Execution

### Milestone 1: Initial Access & Reconnaissance
1. **Reconnaissance:** Inspected `robots.txt` using cURL to discover hidden web paths:
   ```bash
   curl [https://medirozahospital.com/robots.txt](https://medirozahospital.com/robots.txt)

   
