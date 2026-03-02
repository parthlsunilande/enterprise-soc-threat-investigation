# enterprise-soc-threat-investigation
Enterprise SOC Lab: Multi-stage attack investigation using Microsoft Sentinel &amp; Splunk | Brute Force | Phishing | Lateral Movement | Incident Response

# Enterprise SOC Threat Investigation – Security Operations Lab

## Project Title
Enterprise SOC Threat Investigation – Multi-Stage Attack Detection & Incident Response

## Project Overview
This project simulates a real-world enterprise security incident investigated within a Security Operations Center (SOC) environment.
The lab focuses on detecting and responding to a multi-stage attack that includes:
- Brute-force authentication attempts
- Phishing-based credential compromise
- Internal lateral movement and privilege escalation
The investigation was performed using Microsoft Sentinel and Splunk to analyze logs, correlate events, identify Indicators of Compromise (IOCs), and execute a structured incident response process.

## What Problem This Project Solves
Modern enterprises face complex multi-stage attacks that are not always detected through a single alert.
This project demonstrates how a SOC analyst can:
- Detect suspicious authentication activity
- Correlate logs across multiple sources
- Identify malicious patterns
- Trace attacker movement within a network
- Respond using a structured incident response lifecycle
It shows how SIEM tools can be used effectively to investigate and contain enterprise-level threats.

## Technologies Used
- Microsoft Sentinel (KQL queries)
- Splunk (SPL queries)
- Windows Security Event Logs
- Firewall Logs
- Authentication Logs
- MITRE ATT&CK Framework

## How to Install
This project does not require installation of a standalone application.
To replicate this lab environment, you would need:
1. Access to a Microsoft Sentinel workspace  
2. A Splunk instance with Windows log ingestion enabled  
3. Windows Security logs and firewall logs configured for monitoring  
All detection queries are available inside the `Detection-Queries` folder.

## How to Run / Reproduce
1. Ingest Windows Security logs into your SIEM platform.
2. Deploy the provided KQL queries in Microsoft Sentinel.
3. Deploy the provided SPL queries in Splunk.
4. Simulate:
   - Multiple failed login attempts (Event ID 4625)
   - A successful login after failures (Event ID 4624)
   - Privileged account assignment (Event ID 4672)
5. Correlate authentication and firewall logs.
6. Analyze results and document findings.

## Investigation Workflow
1. Alert detection (multiple failed logins)
2. Log correlation across Windows and firewall logs
3. Identification of successful login after brute force
4. Detection of privilege escalation
5. Identification of lateral movement
6. IOC extraction
7. Containment and remediation recommendations
8. Incident documentation

## Screenshots
Screenshots of the investigation dashboard, detection queries, and correlated logs can be found in the `Screenshots` folder.
Example:
![SOC Investigation Overview](https://drive.google.com/drive/u/0/home)

## Indicators of Compromise Identified
- Suspicious external IP address
- Compromised user account
- Abnormal login timestamps
- Internal remote authentication activity

## Security Hardening Recommendations
- Enforce Multi-Factor Authentication (MFA)
- Implement account lockout policies
- Monitor privileged accounts
- Improve SIEM alert tuning
- Enhance log retention and monitoring

## Skills Demonstrated
- SIEM log analysis
- Threat detection & investigation
- Cross-source log correlation
- IOC identification
- Incident response lifecycle execution
- MITRE ATT&CK mapping
- Security hardening strategy

## ⚠ Disclaimer
This project was conducted in a controlled and simulated lab environment for educational and portfolio purposes only.
All logs, IP addresses, usernames, and data have been sanitized.  
No real organizational data has been used.
This repository is intended to demonstrate SOC analyst investigation skills and does not contain any offensive security tools.
