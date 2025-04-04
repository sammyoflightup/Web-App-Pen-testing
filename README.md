# Atlantean Crown Web App Penetration Testing

This repository contains the findings from the web application penetration test performed on Atlantean Crown's web platform. The objective was to assess the security posture of the application, identify vulnerabilities, and provide remediation recommendations.

## Table of Contents:
1. [Introduction](#project-overview)
2. [Information Gathering](#information-gathering)
3. [Vulnerability Scanning](#vulnerability-scanning)
4. [Exploitation](#exploitation)
5. [Recommendations](#recommendations)
6. [Follow-up Testing](#follow-up-testing)

---

## Project Overview

**Target**: Atlantean Crown Web Application  
**Testing Dates**: March, 2025  
**Tester**: Samuel George (Lightup Defence Solution)

### Objective:
The purpose of this penetration test was to assess the security of the Atlantean Crown web application, focusing on identifying potential vulnerabilities that could be exploited by malicious actors.

### Scope:
The test covered all publicly accessible web endpoints, including:
- Authentication mechanisms
- User data storage
- API endpoints
- Third-party integrations

### Methodology:
A combination of automated and manual testing techniques were used to identify security issues such as SQL injection, Cross-Site Scripting (XSS), authentication flaws, and insecure server configurations.

---

## Information Gathering

### Reconnaissance Report

**Domain Information**:
- WHOIS Lookup:  
  ![WHOIS Lookup Screenshot](path/to/whois_screenshot.png)  
- DNS Records:  
  ![DNS Records Screenshot](path/to/dns_screenshot.png)

**Technologies Detected**:
- Web Server: Apache
- CMS: WordPress
- JavaScript Libraries: jQuery, Bootstrap
- Programming Languages: PHP, JavaScript

**Subdomains Identified**:
- api.atlanteancrown.com
- login.atlanteancrown.com

**Nmap Scan**:
- Nmap Scan Screenshot:  
  ![Nmap Scan Screenshot](path/to/nmap_screenshot.png)

---

## Vulnerability Scanning

### Vulnerability Scan Results

**Scanning Tool**: Burp Suite

1. **Vulnerability**: Cross-Site Scripting (XSS)  
   **Description**: Reflected XSS vulnerability in the login form.  
   **Severity**: High  
   **Evidence**: [Insert evidence and payloads]

2. **Vulnerability**: SQL Injection  
   **Description**: Blind SQL Injection detected in the search functionality.  
   **Severity**: Critical  
   **Evidence**: [Insert evidence]

---

## Exploitation

### Exploit Report

1. **Exploit**: Reflected XSS

   **Description**: Successfully executed a payload on the login form that triggered a pop-up, indicating a reflected XSS vulnerability.

   **Impact**: An attacker could steal user sessions or perform actions on behalf of the victim.



---

## Recommendations

1. **XSS Vulnerability**  
   **Recommendation**: Implement proper output encoding and use a Content Security Policy (CSP) to mitigate XSS.

2. **SQL Injection**  
   **Recommendation**: Use prepared statements and parameterized queries to prevent SQL injection attacks.

---

## Follow-up Testing

### Retesting Results

1. **Test**: Reflected XSS  
   **Status**: Fixed.  
   **Description**: The XSS vulnerability was mitigated by implementing input sanitization.

2. **Test**: SQL Injection  
   **Status**: Fixed.  
   **Description**: The SQL injection vulnerability was addressed by using prepared statements.
