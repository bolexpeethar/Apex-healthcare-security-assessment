# Apex-healthcare-security-assessment
Cybersecurity vulnerability assessment of Kioptrix and Metasploitable 2 using Nmap, Nessus Essentials and enum4linux.
[Apex_Healthcare_Security_Assessment_1.0 Group 85 Project (1).pdf](https://github.com/user-attachments/files/35267144/Apex_Healthcare_Security_Assessment_1.0.Group.85.Project.1.pdf)
# Apex Healthcare Solutions – Security Assessment

## Project Overview

This project involved a penetration testing and vulnerability assessment of intentionally vulnerable legacy systems, Kioptrix and Metasploitable 2, within an isolated laboratory environment.

The assessment focused on identifying security weaknesses, evaluating potential risks, documenting technical evidence, and recommending security controls to improve the organization's security posture.

The project was completed as part of a cybersecurity training and group assessment.

## Project Objectives

- Identify exposed network services and potential vulnerabilities.
- Perform network reconnaissance and service enumeration.
- Conduct automated vulnerability scanning.
- Verify identified security weaknesses using scan evidence.
- Assess vulnerabilities based on likelihood and impact.
- Recommend appropriate security controls and policies.

## Lab Environment

| Component | Description |
|---|---|
| Attacking Machine | Kali Linux |
| Target System 1 | Kioptrix |
| Target System 2 | Metasploitable 2 |
| Network Scanning Tool | Nmap |
| Vulnerability Scanner | Nessus Essentials |
| Enumeration Tool | enum4linux |

## Methodology

The assessment followed a structured security testing approach:

1. **Reconnaissance and Host Discovery:** Identified target systems within the isolated lab network.
2. **Port Scanning:** Used Nmap to identify open ports and exposed services.
3. **Service Enumeration:** Identified running services and software versions.
4. **Vulnerability Scanning:** Used Nessus Essentials to identify known security weaknesses.
5. **Manual Verification:** Reviewed scan outputs to validate key findings.
6. **Risk Assessment:** Evaluated vulnerabilities based on likelihood and potential impact.
7. **Security Recommendations:** Proposed appropriate controls to reduce identified risks.

## Key Vulnerabilities Identified

The assessment identified six high-risk findings across the two target systems.

### 1. Kioptrix

**Finding 1: Outdated Apache, mod_ssl and OpenSSL**

- Identified an outdated Apache 1.3.20 web server with mod_ssl 2.8.4 and OpenSSL 0.9.6b.
- These outdated components were associated with known security weaknesses.
- Recommended Control: Upgrade outdated software and implement a formal patch management process.

**Finding 2: SSLv2 Enabled and Weak Encryption**

- Identified SSLv2 support and weak encryption cipher suites on the HTTPS service.
- Weak encryption can expose sensitive information transmitted across a network.
- Recommended Control: Disable SSLv2 and weak cipher suites and enforce modern TLS protocols.

**Finding 3: Exposed Samba Service**

- Identified an exposed Samba service running on TCP port 139.
- The outdated service increased the system's attack surface.
- Recommended Control: Update Samba to a supported version and restrict unnecessary network services.

### 2. Metasploitable 2

**Finding 4: Anonymous FTP Access**

- Identified anonymous FTP login access on TCP port 21.
- The service was running vsftpd 2.3.4.
- Recommended Control: Disable anonymous FTP access and verify software integrity.

**Finding 5: Unencrypted Telnet Service**

- Identified an active Telnet service on TCP port 23.
- Telnet transmits login credentials and session information in plaintext.
- Recommended Control: Disable Telnet and replace it with SSH for secure remote administration.

**Finding 6: Anonymous/Null SMB Session Enumeration**

- Used enum4linux to identify SMB access through a blank username and password.
- The configuration exposed information about user accounts and shared folders.
- Recommended Control: Restrict null sessions and enforce authenticated, least-privilege SMB access.

## Tools and Technologies Used

| Tool | Purpose |
|---|---|
| Kali Linux | Security assessment platform |
| Nmap | Host discovery, port scanning and service/version detection |
| Nessus Essentials | Automated vulnerability scanning |
| enum4linux | SMB enumeration and share discovery |
| Kioptrix | Intentionally vulnerable assessment environment |
| Metasploitable 2 | Intentionally vulnerable assessment environment |

## Risk Assessment

The identified vulnerabilities were evaluated based on their likelihood of exploitation and potential impact.

All six findings received an overall High-risk rating.

The assessment highlighted weaknesses involving:

- Outdated software and unsupported services.
- Weak encryption protocols.
- Inadequate access controls.
- Anonymous access to network services.
- Exposure of sensitive system information.

## Recommended Security Controls

The following controls were recommended to improve the security posture:

1. **Patch Management:** Regularly update operating systems, applications and services.
2. **Access Control:** Restrict system access to authorized users.
3. **Vulnerability Management:** Conduct regular security scans and track remediation.
4. **Password and Authentication Policy:** Enforce strong authentication and secure access practices.
5. **Protocol Hardening:** Disable insecure protocols such as SSLv2 and Telnet.
6. **Service Minimization:** Disable unnecessary network services and restrict exposed ports.

## Project Outcomes and Learning Experience

Through this assessment, I gained practical experience in:

- Network reconnaissance and port scanning.
- Identifying open ports and running services.
- Vulnerability scanning and verification.
- SMB enumeration and service analysis.
- Understanding vulnerability severity and risk ratings.
- Developing security recommendations and preventive controls.
- Documenting technical findings in a professional security assessment report.

## Disclaimer

This assessment was conducted within an authorized, isolated laboratory environment using intentionally vulnerable systems, Kioptrix and Metasploitable 2.

No testing was performed against real healthcare infrastructure or unauthorized systems. No exploitation was performed against either target during this assessment.

## Project Report

The complete security assessment report, including technical findings and supporting screenshots, is available below:

[View Full
