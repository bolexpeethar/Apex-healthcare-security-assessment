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
<img width="960" height="540" alt="WhatsApp Image 2026-11-23 at 9 53 39 PM" src="https://github.com/user-attachments/assets/c97a5e3e-9860-4b8d-aae9-ff526715de54" />
<img width="960" height="540" alt="WhatsApp Image 2026-11-23" src="https://github.com/user-attachments/assets/25a1cb07-72b7-4ed3-816a-5293ab63defd" />
<img width="960" height="540" alt="WhatsApp Image 2026-11-23 at 9 53 39" src="https://github.com/user-attachments/assets/013c4ead-7e75-4b76-b8a2-311d994cc14a" />
<img width="1280" height="720" alt="WhatsApp Image 2026-11-23 at 9 53 40" src="https://github.com/user-attachments/assets/c750a92f-a7f0-41d8-9ad3-155183c2b927" />
<img width="756" height="1008" alt="WhatsApp Image 2026-11-23 at 9 53 40 " src="https://github.com/user-attachments/assets/5888c423-1838-4a06-8ee6-c99f19784f56" />
<img width="756" height="1008" alt="WhatsApp Image 2026-11-23 at 9 53 41 " src="https://github.com/user-attachments/assets/3831aae7-b751-4848-862a-a37948623a83" />
<img width="756" height="1008" alt="WhatsApp Image 2026-11-23 at 9 53 42" src="https://github.com/user-attachments/assets/48da2ad9-feb3-4be9-bc17-52fe656c272b" />
<img width="756" height="1008" alt="WhatsApp Image 2026-11-23 at 9 53 42 " src="https://github.com/user-attachments/assets/2457b177-3301-4f2c-bd6e-c89ba49d5156" />
<img width="756" height="1008" alt="WhatsApp Image 2026-11-23 at 9 53 42 PM" src="https://github.com/user-attachments/assets/d24e0041-2235-459f-af1c-71f9589b7f84" />
<img width="756" height="1008" alt="WhatsApp Image 2026-11-23 at 9 53 43 PM" src="https://github.com/user-attachments/assets/f354195b-2aae-4c9f-afa0-829c2716f8c1" />
<img width="756" height="1008" alt="WhatsApp Image 2026-11-23 at 9 53 43 " src="https://github.com/user-attachments/assets/cf4d05e1-f4fe-428b-ad9d-a9af185a9ccc" />
<img width="756" height="1008" alt="WhatsApp Image 2026-11-23 at 9 53 44 PM" src="https://github.com/user-attachments/assets/0cc373d5-e559-490e-84f9-4c71ddb5d6bc" />
<img width="1008" height="756" alt="WhatsApp Image 2026-11-23 at 9 53 45 PM" src="https://github.com/user-attachments/assets/9acc75a7-9c7a-4426-9db2-d894b1854450" />
<img width="1008" height="756" alt="WhatsApp Image 2026-11-23 at 9 53 45" src="https://github.com/user-attachments/assets/74b7f06e-afc1-4d0d-af95-a97d53e4c867" />
<img width="1008" height="756" alt="WhatsApp Image 2026-11-23 at 9 53 4" src="https://github.com/user-attachments/assets/530ef71e-5b8c-4223-bb7f-dd951b6bd144" />
<img width="960" height="1280" alt="WhatsApp Image 2026-11-23 at 10 42 50 PM" src="https://github.com/user-attachments/assets/4f41e19d-a4ae-48ae-8eac-fc05889a5f68" />
<img width="960" height="1280" alt="WhatsApp Image 2026-11-23 at 10 42 51 PM" src="https://github.com/user-attachments/assets/2b30d761-b42e-461b-a9d5-d2f2cecc8740" />
<img width="960" height="1280" alt="WhatsApp Image 2026-11-23 at 10 42 50 " src="https://github.com/user-attachments/assets/7855cf54-c639-408f-84cd-ee3719854235" />
<img width="960" height="1280" alt="WhatsApp Image 2026-11-23 at 10 42 5" src="https://github.com/user-attachments/assets/04bbbbe6-e010-4313-80c6-3e8f6e15b0e9" />
<img width="960" height="1280" alt="WhatsApp Image 2026-11-23 at 10 42" src="https://github.com/user-attachments/assets/8b00fabe-1c6c-468f-ab78-77c33ab2152e" />



