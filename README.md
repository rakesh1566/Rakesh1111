# Rakesh1111# Web Application & API Security Assessment Methodology

This repository contains my personal testing checklist and methodology for Web Application Security and API Assessments based on OWASP Top 10 guidelines.

---

## 🌐 Web Application Security Checklist (OWASP Top 10)

### 1. Information Gathering & Reconnaissance
* [ ] Subdomain Enumeration (Amass, Subfinder)
* [ ] Port Scanning & Service Fingerprinting (Nmap)
* [ ] Directory & File Brute-Forcing (ffuf, Gobuster)
* [ ] Content Management System (CMS) Analysis

### 2. Authentication & Session Management
* [ ] Username Enumeration & Password Spraying
* [ ] Weak Password Policies & Multi-Factor Authentication (MFA) Bypasses
* [ ] Session Fixation & Weak Session Token Generation
* [ ] Cookie Security Attributes (HttpOnly, Secure, SameSite)

### 3. Authorization & Access Control
* [ ] Insecure Direct Object References (IDOR / BOLA)
* [ ] Privilege Escalation (Horizontal & Vertical)
* [ ] Cross-Site Request Forgery (CSRF)

### 4. Injection Vulnerabilities
* [ ] SQL Injection (In-band, Blind, Time-based)
* [ ] Cross-Site Scripting (Reflected, Stored, DOM-based XSS)
* [ ] Server-Side Template Injection (SSTI)
* [ ] Command Injection & Local/Remote File Inclusion (LFI/RFI)

### 5. Server-Side Request Forgery (SSRF)
* [ ] Out-of-band SSRF testing on HTTP headers & URL parameters
* [ ] Internal IP scanning via cloud metadata endpoints (`169.254.169.254`)

---

## 🔌 API Testing Steps (OWASP API Security Top 10)

### 1. API Reconnaissance & Endpoint Discovery
* [ ] Import OpenAPI/Swagger documentation into Postman or Burp Suite
* [ ] Hidden API endpoint discovery (`/api/v1`, `/api/v2`, `/graphql`)

### 2. Broken Object Level Authorization (BOLA)
* [ ] Test parameter manipulation on IDs (`/api/users/101` -> `/api/users/102`)
* [ ] Test access across different user roles

### 3. Broken Authentication & Mass Assignment
* [ ] Inspect JWT token signature validation and weak algorithms (`alg: none`)
* [ ] Test Mass Assignment by adding unauthorized JSON fields (`"is_admin": true`)

### 4. Rate Limiting & Resource Consumption
* [ ] Brute-force endpoint without rate limit (OTP, login attempts)
* [ ] Test for GraphQL Query Depth / Batching attacks

---

## 🛠️ Preferred Toolset
* **Burp Suite Professional** (Proxy, Intruder, Repeater)
* **Postman** (API Endpoint Testing)
* **ffuf / Gobuster** (Fuzzing)
* **Nmap** (Network Scanning)
* **Nuclei** (Automated Vulnerability Scanning)

---
*Maintained by Independent Security Researcher for vulnerability hunting and crowd-sourced assessments.*
