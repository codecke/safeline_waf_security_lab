# safeline_waf_security_lab
A hands-on web application security lab demonstrating the deployment of SafeLine WAF in front of a deliberately vulnerable DVWA application, with attack simulation and defensive testing using Kali Linux.



# SafeLine WAF & DVWA Web Application Security Lab

![Cybersecurity](https://img.shields.io/badge/Focus-Web%20Application%20Security-red)
![WAF](https://img.shields.io/badge/WAF-SafeLine-blue)
![Linux](https://img.shields.io/badge/Linux-Ubuntu%20%7C%20Kali-orange)
![Status](https://img.shields.io/badge/Status-Completed-success)

## Overview

This project involved designing and deploying a controlled web application security lab to explore how a Web Application Firewall (WAF) can protect a vulnerable web application from common web-based attacks.

The lab was built using SafeLine WAF, DVWA (Damn Vulnerable Web Application), Ubuntu Linux, Kali Linux, Apache, MariaDB, and VirtualBox.

The primary objective was to deploy DVWA behind SafeLine as a reverse-proxy WAF, simulate attacks from Kali Linux, and observe how SafeLine detects, blocks, and rate-limits malicious traffic.

---

## Project Objectives

The main objectives of this project were to:

- Build an isolated cybersecurity testing environment.
- Deploy DVWA as a deliberately vulnerable web application.
- Configure Apache as the backend web server.
- Configure MariaDB as the DVWA database backend.
- Deploy SafeLine as a Web Application Firewall.
- Configure SafeLine as a reverse proxy in front of DVWA.
- Configure HTTPS and SSL for secure access.
- Simulate common web application attacks from Kali Linux.
- Test SafeLine's ability to detect and block malicious traffic.
- Configure and test HTTP flood protection and rate limiting.
- Analyze the results of security tests.
- Gain practical experience with web application security architecture.

---

## Lab Architecture

The final architecture consisted of three major components:

1. Kali Linux – Attack simulation environment
2. SafeLine WAF – Security and traffic inspection layer
3. Ubuntu – Backend application server hosting Apache and DVWA

![Lab Architecture](architecture/lab-architecture.png)

### Traffic Flow

```text
Kali Linux
Attack Simulation
      |
      | HTTPS :443
      v
SafeLine WAF
      |
      | Reverse Proxy
      v
Apache :8080
      |
      v
DVWA
      |
      v
MariaDB
