# Cybersecurity Portfolio

A curated collection of academic and hands-on cybersecurity work focused on penetration testing, incident response, and ransomware case analysis. These projects reflect practical skills in vulnerability discovery, exploitation workflow, incident handling, containment strategy, recovery planning, and security reporting.

---

## Projects Overview

| Project | Focus Area | Core Skills Demonstrated |
| --- | --- | --- |
| Kali + Metasploitable 2 Exploitation Lab | Penetration Testing | Network discovery, service enumeration, exploit selection, Metasploit configuration, controlled exploitation |
| CDK Global Ransomware Case Study | Incident Analysis | Timeline reconstruction, impact analysis, response evaluation, root cause analysis, recommendations |
| Zenith Tech Ransomware IR Activity | Incident Response | Detection, triage, containment, eradication, recovery, compliance reporting, post-incident review |

---

## 1) Kali Linux and Metasploitable 2 Exploitation Lab

### Project Summary
This lab documents a structured exploitation workflow carried out from Kali Linux against a Metasploitable 2 virtual machine. The exercise focused on identifying a reachable target, confirming live hosts, locating a vulnerable service, selecting the correct Metasploit module for VSFTPD v2.3.4, configuring required options, and successfully executing the exploit to gain control of the target system.

### Objective
To demonstrate the end-to-end offensive security process used in a controlled lab environment:
- Discover hosts on the local network
- Validate connectivity between attacker and target
- Identify a vulnerable service and version
- Find and load a matching Metasploit exploit
- Configure exploit options correctly
- Execute exploitation and verify access

### Highlights
- Used network discovery techniques to identify active systems
- Confirmed connectivity between Kali and the Metasploitable VM
- Located and loaded the `vsftpd_234` Metasploit module
- Verified configuration with `show options`
- Executed the exploit and confirmed control of the target system

### Skills Demonstrated
`Kali Linux` `Metasploit` `Network Discovery` `fping` `Service Enumeration` `Exploit Selection` `Exploit Configuration` `VSFTPD 2.3.4`

### Key Takeaway
This project shows practical understanding of how exploitation happens in real environments: reconnaissance, vulnerable service identification, exploit matching, configuration, and execution. It also highlights the business risk created by exposed and unpatched services.

---

## 2) CDK Global Ransomware Incident Case Study

### Project Summary
This case study analyzes the June 2024 ransomware attacks on CDK Global, a major dealer-management software provider serving approximately 15,000 dealerships across North America. The report reconstructs the incident timeline, evaluates containment and recovery decisions, examines likely contributing factors, and presents lessons learned and prioritized recommendations.

### Executive Overview
The incident involved two ransomware attacks within roughly 24 hours, causing widespread operational disruption across dealerships that depended on CDK’s platform. Dealers were forced into manual workflows for nearly two weeks. Reported financial consequences included an estimated dealer loss of about USD 1.02 billion, while multiple reports indicated a ransom payment of approximately USD 25 million in Bitcoin.

### Scope of Analysis
- Incident overview and timeline
- Business, operational, and reputational impact
- Containment, eradication, and recovery assessment
- Root cause and contributing factors
- Strategic recommendations for resilience improvement

### Notable Findings
- Rapid shutdown likely limited further spread after detection
- A second attack during recovery suggested eradication was incomplete
- Dependence on ransom payment exposed weak recovery independence
- Shared or weakly segmented remote-access architecture increased concentration risk
- The event demonstrated how compromise of a single SaaS provider can disrupt an entire industry

### Recommendations Highlighted in the Report
- Independently verify eradication before reconnecting systems
- Replace shared access models with segmented, zero-trust, MFA-protected connectivity
- Maintain regularly tested backups and rehearse business continuity procedures

### Skills Demonstrated
`Ransomware Analysis` `Incident Timeline Reconstruction` `Business Impact Assessment` `Root Cause Analysis` `Critical Evaluation` `Security Recommendations` `Cybersecurity Writing`

### Key Takeaway
This project demonstrates the ability to move beyond incident description into analytical security reporting: assessing what failed, what worked, what the downstream business impact was, and what should change to reduce recurrence.

---

## 3) Zenith Tech Ransomware Incident Response Activity

### Project Summary
This report presents a detailed incident response walkthrough for a ransomware scenario at Zenith Tech. Structured around recognized incident-handling practices, the work documents actions taken from preparation through post-incident review, including the specific commands, tools, and decisions used during the response.

### Incident Snapshot
- Incident type: Ransomware attempt
- Initial compromise vector: Phishing email with malicious macro content
- Detection time: 09:00
- Full recovery achieved: 12:22
- Total incident duration: 3 hours, 42 minutes
- Outcome: Operations restored without confirmed data encryption or exfiltration

### Response Workflow Covered
#### Preparation
The environment already had SIEM alerts, endpoint detection and response coverage, immutable offline backups, and forensic tooling in place. These controls enabled fast detection and quick authority to isolate systems.

#### Identification
The incident was detected through a SIEM alert showing suspicious outbound traffic and abnormal file-renaming activity on host `ZT-WKS01`. Authentication logs, endpoint telemetry, and threat intelligence checks were used to validate the threat and classify the incident as critical.

#### Containment
The response included:
- Disabling the affected switch port
- Moving the impacted VLAN into quarantine
- Disabling the compromised Active Directory account
- Resetting Kerberos tickets
- Blocking malicious command-and-control destinations at the firewall
- Capturing memory and disk images for evidence preservation

#### Eradication
The team:
- Identified the malware through behavior and hash evidence
- Removed persistence mechanisms
- Traced the entry vector to a phishing email received at 08:40
- Purged the email from mailboxes
- Blocked the sender domain
- Re-imaged the compromised workstation from a known-clean image
- Ran EDR scans across the affected VLAN
- Rotated impacted credentials and enforced MFA

#### Recovery
The response restored customer data from immutable backups, validated restoration integrity through row counts and checksums, re-enabled internal systems, and returned the business to normal operations.

#### Post-Incident and Compliance
The report also included communication planning, management notification, and preparation of an OSFI-style report within the required reporting window, along with post-incident improvements such as stronger attachment sandboxing and updated threat intelligence.

### Skills Demonstrated
`Incident Response` `SIEM` `EDR` `Forensics` `Active Directory` `Firewall Containment` `Backup Validation` `Phishing Analysis` `MFA Enforcement` `Compliance Reporting`

### Key Takeaway
This project reflects operational incident response thinking: preserve evidence, stop spread quickly, remove persistence, rebuild from trusted sources, validate recovery, and capture lessons learned for long-term resilience.

---

## Tools and Platforms Referenced
- Kali Linux
- Metasploit Framework
- Metasploitable 2
- SIEM
- EDR
- Active Directory
- Firewall controls
- FTK Imager
- Magnet RAM Capture
- Backup and restore tooling

---

## Portfolio Value
These reports together show a balanced cybersecurity profile across offensive and defensive practice:
- **Offensive security:** discovery, exploitation workflow, vulnerability validation
- **Defensive operations:** detection, containment, eradication, recovery, reporting
- **Security analysis:** case-study evaluation, lessons learned, and risk reduction planning

They also demonstrate strong written communication for technical reporting, which is essential for analysts, SOC teams, incident responders, and junior security consultants.

---

## Author
**Olumide Akomolafe**

Cybersecurity student portfolio featuring lab work, incident analysis, and response documentation.
