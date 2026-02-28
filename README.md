# Vulnerability Assessment Report - Live Website (Task 1)

## 📌 Project Overview
This project was completed as part of a Cyber Security internship. The goal was to conduct a comprehensive **Vulnerability Assessment** on the live test environment `testphp.vulnweb.com` to identify potential security flaws and system misconfigurations.

---

## 🛠️ Tools & Methodology
The assessment followed a structured approach using industry-leading tools:
* **Nmap (Zenmap):** Used for service fingerprinting and identifying open ports (e.g., Port 80/HTTP).
* **OWASP ZAP (Passive Scanning):** Employed to detect common web vulnerabilities without active exploitation.
* **Browser DevTools:** Utilized for manual HTTP response header analysis and identifying information disclosure.
* **Documentation:** Final report designed using Canva/MS Word to communicate findings effectively.

---

## 🔍 Key Security Findings
The following vulnerabilities were identified and documented in the final report:

### 1. Outdated Software (High Risk) 🔴
* **Issue:** The web server is running **PHP 5.6.40** and **nginx 1.19.0**.
* **Impact:** These versions are no longer supported and contain multiple known CVEs (Common Vulnerabilities and Exposures).

### 2. Missing Security Headers (Medium Risk) 🟠
* **Issue:** Missing `X-Frame-Options` and `Content-Security-Policy` (CSP).
* **Impact:** Increases the risk of **Clickjacking** and **Cross-Site Scripting (XSS)** attacks.

### 3. Lack of Anti-CSRF Protection (Medium Risk) 🟠
* **Issue:** Forms on the site do not implement unique anti-CSRF tokens.
* **Impact:** Attackers can trick authenticated users into performing unwanted actions.

---

## 🛡️ Remediation Strategy
* **Update Stack:** Upgrade the server to use a supported version of PHP (e.g., 8.x).
* **Secure Headers:** Implement a strict `Content-Security-Policy` and `Strict-Transport-Security`.
* **Token Validation:** Add unique per-session CSRF tokens to all web forms.

---

## 📄 Deliverables
* **[Vulnerability_Assessment_Report.pdf](./Vulnerability_Assessment_Report.pdf):** Detailed technical report with evidence and risk classification.
