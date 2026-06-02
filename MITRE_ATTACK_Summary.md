# MITRE ATT&CK Techniques Summary: T1059, T1078, and T1566

## Overview

The MITRE ATT&CK framework is a knowledge base of adversary tactics and techniques based on real-world observations. Security Operations Center (SOC) analysts use ATT&CK to understand attacker behavior, improve detection capabilities, and strengthen defensive strategies. This summary focuses on three commonly observed techniques: T1059 (Command and Scripting Interpreter), T1078 (Valid Accounts), and T1566 (Phishing).

---

## T1059 – Command and Scripting Interpreter

**Tactic(s):** Execution

T1059 describes the use of command-line interfaces and scripting languages to execute malicious code on a target system. Attackers often leverage legitimate tools such as PowerShell, Command Prompt (cmd.exe), Bash, Python, or other scripting environments to perform actions without introducing obvious malware.

### Common Uses

* Running malicious commands remotely.
* Downloading and executing payloads.
* Automating reconnaissance and persistence activities.
* Evading detection by using trusted system utilities.

### Detection Opportunities

* Monitor unusual PowerShell or command-line activity.
* Identify encoded or obfuscated commands.
* Alert on execution of scripts from suspicious locations.
* Correlate command execution with other malicious events.

### Mitigation

* Restrict script execution where possible.
* Implement application allowlisting.
* Enable detailed PowerShell and command-line logging.
* Apply least-privilege access controls.

---

## T1078 – Valid Accounts

**Tactic(s):** Initial Access, Persistence, Privilege Escalation, Defense Evasion

T1078 occurs when attackers gain access to legitimate user or service accounts and use them to operate within an environment. Since the credentials are valid, malicious activity may appear normal and can bypass some security controls.

### Common Uses

* Accessing corporate networks with stolen credentials.
* Maintaining persistence after compromise.
* Moving laterally between systems.
* Accessing cloud services and administrative interfaces.

### Detection Opportunities

* Monitor unusual login locations or times.
* Detect impossible travel events.
* Identify excessive failed authentication attempts.
* Review privilege escalation and account modification events.

### Mitigation

* Enforce multi-factor authentication (MFA).
* Use strong password policies.
* Monitor privileged account activity.
* Regularly audit and disable unused accounts.

---

## T1566 – Phishing

**Tactic(s):** Initial Access

T1566 involves deceiving users into opening malicious attachments, clicking harmful links, or revealing credentials. Phishing remains one of the most successful initial access techniques because it targets human behavior rather than technical vulnerabilities.

### Common Uses

* Credential theft.
* Malware delivery.
* Business email compromise (BEC).
* Establishing an initial foothold in a network.

### Detection Opportunities

* Analyze email attachments and embedded links.
* Monitor for suspicious sender domains.
* Detect unusual authentication events following email activity.
* Use email security gateways and threat intelligence feeds.

### Mitigation

* Conduct regular security awareness training.
* Implement email filtering and sandboxing.
* Enable MFA to reduce credential abuse risk.
* Encourage prompt reporting of suspicious emails.

---

## Conclusion

T1059, T1078, and T1566 represent critical techniques frequently observed in real-world cyber incidents. Together they illustrate a common attack chain: phishing (T1566) provides initial access, stolen or compromised credentials enable valid account abuse (T1078), and command or scripting interpreters (T1059) facilitate execution of malicious actions. Understanding these techniques helps SOC analysts improve detection, response, and overall defensive readiness.
