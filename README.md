# Atlantean Crown Web App Penetration Testing

This repository contains the findings from the web application penetration test performed on Atlantean Crown's web platform. The objective was to assess the security posture of the application, identify vulnerabilities, and provide remediation recommendations.

---

## Table of Contents

1. [Project Overview](#project-overview)  
2. [Information Gathering](#information-gathering)  
3. [Vulnerability Scanning](#vulnerability-scanning)  
4. [Exploitation](#exploitation)  
5. [Recommendations](#recommendations)  
6. [Follow-up Testing](#follow-up-testing)  

---

## Project Overview

**Target:** Atlantean Crown Web Application  
**Testing Dates:** March, 2025  
**Tester:** Samuel George (Lightup Defence)

### Objective  
The purpose of this penetration test was to assess the security of the Atlantean Crown web application, focusing on identifying potential vulnerabilities that could be exploited by malicious actors.

### Scope  
The test covered all publicly accessible web endpoints, including:  
- Authentication mechanisms  
- User data storage  
- API endpoints  
- Third-party integrations

### Methodology  
A combination of automated and manual testing techniques were used to identify security issues such as SQL injection, Cross-Site Scripting (XSS), authentication flaws, and insecure server configurations.

---

## Information Gathering

### Reconnaissance Report

**Domain Information:**  
![WhatsApp Image 2025-08-07 at 6 21 47 PM (1)](https://github.com/user-attachments/assets/7733aa90-8770-4220-bacd-7998e7e8a4a2)
![WhatsApp Image 2025-08-07 at 6 21 47 PM](https://github.com/user-attachments/assets/c7945b1a-4a37-4bc0-b5d4-45cb525fca6e)


**Technologies Detected:**  
- Web Server: Apache  
- CMS: WordPress  
- JavaScript Libraries: jQuery, Bootstrap  
- Programming Languages: PHP, JavaScript

**Subdomains Identified:**  
- api.atlanteancrown.com  
- login.atlanteancrown.com

**Nmap Scan:**  
- Nmap Scan Screenshot:  
  ![Nmap Scan Screenshot](path/to/nmap_screenshot.png)

---

## Vulnerability Scanning

### Vulnerability Scan Results

**Scanning Tool:** Burp Suite

1. **Vulnerability:** Cross-Site Scripting (XSS)  
   - **Description:** Reflected XSS vulnerability in the login form.  
   - **Severity:** High  
   - **Evidence:** [Insert evidence and payloads here]

2. **Vulnerability:** SQL Injection  
   - **Description:** Blind SQL Injection detected in the search functionality.  
   - **Severity:** Critical  
   - **Evidence:** [Insert evidence here]

---

## Exploitation

### Exploit Report

1. **Exploit:** Reflected XSS  
   - **Description:** Successfully executed a payload on the login form that triggered a pop-up, indicating a reflected XSS vulnerability.  
   - **Impact:** An attacker could steal user sessions or perform actions on behalf of the victim.

---

## Recommendations

1. **XSS Vulnerability**  
   - **Recommendation:** Implement proper output encoding and use a Content Security Policy (CSP) to mitigate XSS.

2. **SQL Injection**  
   - **Recommendation:** Use prepared statements and parameterized queries to prevent SQL injection attacks.

---

## Follow-up Testing

### Retesting Results

1. **Test:** Reflected XSS  
   - **Status:** Fixed.  
   - **Description:** The XSS vulnerability was mitigated by implementing input sanitization.

2. **Test:** SQL Injection  
   - **Status:** Fixed.  
   - **Description:** The SQL injection vulnerability was addressed by using prepared statements.

---
