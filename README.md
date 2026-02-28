​Vulnerability Assessment Report - Live Website (Task 1)
​📌 Project Overview
​This project is part of my Cyber Security internship. The objective was to perform a comprehensive Vulnerability Assessment on a live test website (testphp.vulnweb.com) to identify security weaknesses, outdated software, and misconfigurations.
​🛠️ Tools Used
​To ensure a thorough analysis, the following industry-standard tools were utilized:
​Nmap (Zenmap): Used for network discovery, port scanning, and service version fingerprinting.
​OWASP ZAP (Passive Scan): Employed for automated vulnerability identification, specifically looking for missing security headers and CSRF issues.
​Browser DevTools: Used for manual inspection of HTTP response headers and identifying information leakage.
​Canva / MS Word: Used for professional report design and documentation.
​🔍 Key Findings
​During the assessment, several critical and medium-level vulnerabilities were identified:
​Outdated Software: The server is running an obsolete version of PHP (5.6.40), which is prone to numerous known exploits (CVEs).
​Missing Security Headers: Critical protection headers like X-Frame-Options (Anti-Clickjacking) and Content-Security-Policy are absent.
​Lack of Anti-CSRF Tokens: Forms on the website do not use unique tokens, making users vulnerable to Cross-Site Request Forgery attacks.
​Information Disclosure: The X-Powered-By header reveals exact backend technology versions to potential attackers.
​🛡️ Remediation Recommendations
​Upgrade Technology Stack: Migrate from PHP 5.6 to a modern, supported version like PHP 8.x.
​Implement Security Headers: Configure the web server to include Strict-Transport-Security and X-Content-Type-Options: nosniff.
​Form Protection: Integrate unique CSRF tokens for all state-changing requests.
​📄 Deliverables
​Vulnerability_Report.pdf: A professionally designed report containing detailed findings, screenshots (PoC), and risk classifications (Low/Medium/High).
