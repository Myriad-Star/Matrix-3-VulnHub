
# Matrix 3 - VulnHub Walkthrough

## Overview

This repository documents my penetration-testing walkthrough of **Matrix 3**, a vulnerable virtual machine from VulnHub.

The objective was to identify vulnerabilities, obtain initial access, escalate privileges, and ultimately gain root access.

## Lab Information

| Category | Details |
|---|---|
| Machine | Matrix 3 |
| Platform | VulnHub |
| Attacker | Kali Linux |
| Target IP | 192.168.1.11 |
| Open Ports | 80, 6464, 7331 |
| Initial Access | SSH |
| Privilege Escalation | SSH key injection and sudo misconfiguration |
| Final Access | Root |

## Attack Methodology

1. **Reconnaissance:** Identified open ports and running services using Nmap.
2. **Web Enumeration:** Investigated web services, directories, and hidden resources.
3. **Credential Discovery:** Retrieved credentials from a hidden file and a .NET executable.
4. **Initial Access:** Obtained SSH access as the guest user.
5. **Privilege Escalation:** Abused a permitted sudo copy command to gain access as Trinity.
6. **Root Access:** Exploited a sudo rule allowing Trinity to execute a user-controlled script as root.

## Repository Structure

- `reconnaissance/` – Target discovery and service enumeration.
- `enumeration/` – Web investigation and credential discovery.
- `initial-access/` – Initial SSH access.
- `privilege-escalation/` – Guest-to-Trinity and Trinity-to-root escalation.
- `screenshots/` – Supporting evidence.

## Disclaimer

This walkthrough was conducted in an isolated, intentionally vulnerable lab environment for educational purposes. All techniques are documented for cybersecurity learning and authorized security testing.
