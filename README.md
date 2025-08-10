# Task 3 — Basic Vulnerability Scan on Local Machine

## Objective
Use Nessus Essentials to identify common vulnerabilities on my local Windows 11 machine.

## Tools Used
- Nessus Essentials (Free Vulnerability Scanner)
- Windows 11 (Scan Target)

##  Steps Taken
1. Installed Nessus Essentials and activated with a free license.
2. Created a **Basic Network Scan** targeting my local IP: `192.168.0.102`.
3. Launched the scan and waited for results (approx. 18 minutes).
4. Reviewed vulnerabilities and their CVSS scores.
5. Researched remediation steps for the most critical issues.

## Screenshots
### Scan Summary
![Scan Summary](scan-summary.png)

### Vulnerability Details
![Vulnerability Details](vulnerability-details.png)

##  Key Findings
| Severity | Vulnerability Name              | CVSS | Description | Recommended Fix |
|----------|----------------------------------|------|-------------|-----------------|
| Medium   | SMB Signing not required         | 5.3  | Allows attackers to modify SMB traffic without detection. | Enable SMB signing in Windows Group Policy. |
| Mixed    | SSL (Multiple Issues)            | N/A  | Weak or outdated SSL/TLS configurations. | Disable outdated SSL/TLS versions, enable TLS 1.2/1.3. |
| Info     | SMB (Multiple Issues)            | N/A  | General SMB protocol information disclosures. | Review and disable unused SMB shares. |

## Conclusion
The scan revealed configuration weaknesses in SMB and SSL settings.  
Mitigation steps involve enabling SMB signing, updating SSL/TLS configurations, and disabling insecure services.
