## SOC Incident Report: Brute Force Attack Detection (Hydra)

## Overview

This report documents a simulated brute force attack performed from a Kali Linux machine targeting a Windows 10 system. The attack was successfully detected and analyzed using the Wazuh SIEM platform.

---

## Objective

- Simulate a brute force attack using Hydra
- Monitor authentication logs
- Detect and analyze attack behavior in Wazuh
- Generate a professional SOC incident report

---

## Lab Environment

Attacker Machine- Kali Linux
Target Machine- Windows 10
SIEM Tool- Wazuh
Virtualization- VirtualBox

---

## Attack Description

A brute force attack was executed using Hydra against the target system by attempting multiple password combinations from a predefined wordlist.

---

## Detection in Wazuh

Observations

- Multiple failed login attempts detected
- Event ID: 4625 (Failed Login Attempts)
- No successful login initially
- Total failed attempts observed: 10+

## Log Indicators

- Repeated authentication failures from a single IP
- High frequency login attempts
- Suspicious pattern indicating brute force attack

---

## Alert Details

Rule Triggered- Authentication Failure
Event ID- 4625
Severity Level- 5 Medium 
Source IP- 192.168.X.X
Target System- Windows 10

---

## Analysis

The attack pattern clearly indicates a brute force attempt:

- Multiple login failures within a short time
- Automated tool behavior (Hydra)
- Consistent username with varying passwords

This confirms a password guessing attack targeting the system.

---

## Impact

- Risk of unauthorized access
- Potential compromise of user credentials
- System exposure to further attacks

---

## Mitigation & Recommendations

Immediate Actions

- Block attacker IP address
- Disable or lock targeted account
- Enable account lockout policies

Long-Term Security Improvements

- Implement strong password policies
- Enable Multi-Factor Authentication (MFA)
- Monitor login attempts continuously
- Configure SIEM alerts for brute force detection

---

## Lessons Learned

- Brute force attacks are easily detectable with proper monitoring
- SIEM tools like Wazuh provide real-time visibility
- Log analysis is critical for SOC analysts

---

## Conclusion

The brute force attack was successfully simulated and detected using Wazuh. This exercise demonstrates how SOC analysts can identify and respond to authentication-based attacks effectively.

---

#### Author

SOC Analyst (Beginner Lab Project)
Ganesh

---
