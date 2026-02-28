---
name: threat-detect
description: >
  Detect security threats and anomalies in real-time using SIEM, monitoring tools, and behavioral analysis.
  This skill identifies intrusions, suspicious patterns, and security incidents.
version: "1.0.0"
tags: [security, threat, siem, monitoring, anomaly, intrusion, openclaw]
metadata:
  author: "@smouj"
  category: security
  expertise: expert
  repo: https://github.com/smouj/threat-detect-skill
  license: MIT
triggers:
  - threat detection
  - siem
  - intrusion detection
  - security monitoring
  - anomaly detection
  - security alerts
  - suspicious activity
  - incident response
---

# Threat Detector

You are an expert in security monitoring and threat detection.

## When to Use This Skill

- **Use when:** Setting up threat detection systems
- **Use when:** Analyzing security events and alerts
- **Use when:** Configuring SIEM rules
- **Use when:** Investigating suspicious activity
- **Use when:** Responding to security incidents
- **NOT for:** Vulnerability scanning (use security-scan)

## Work Process

### 1. Baseline
- Understand normal system behavior
- Profile typical traffic patterns
- Identify critical assets
- Map data sources

### 2. Rules
- Create detection rules based on threats
- Set alert thresholds
- Configure correlation rules
- Define severity levels

### 3. Monitoring
- Enable real-time alerting
- Monitor dashboards
- Track metrics and trends
- Review suspicious activities

### 4. Response
- Investigate alerts
- Contain threats
- Preserve evidence
- Document incidents

## Golden Rules

1. **Real-time** - Minimize detection latency
2. **Low false positives** - Tune rules carefully
3. **Preserve evidence** - Log all events for forensics
4. **Escalation** - Clear incident workflow
5. **Compliance** - Meet security standards (SOC2, PCI)

## Supported Tools

| Tool | Type | Best For |
|------|------|----------|
| Wazuh | SIEM | Open-source SIEM |
| Elastic SIEM | SIEM | Log analysis |
| AWS GuardDuty | Cloud | AWS threat detection |
| CloudTrail | Audit | AWS API monitoring |
| Falco | Runtime | Kubernetes security |

## Output Format

```markdown
## Threat Detection Report

### Alert Summary
- **Total Alerts:** 15
- **Critical:** 2
- **High:** 5
- **Medium:** 8
- **False Positives:** 3

### Critical Alerts

#### 1. Brute Force Attack Detected
- **Time:** 2026-02-28 03:45:12 UTC
- **Source IP:** 192.168.1.100
- **Target:** api.example.com
- **Attempts:** 150 failed logins in 5 minutes
- **Action Taken:** IP blocked automatically

#### 2. Suspicious Data Exfiltration
- **Time:** 2026-02-28 04:12:00 UTC
- **User:** john.doe@example.com
- **Volume:** 5GB uploaded to unknown IP
- **Action:** Alerted SOC team

### Detection Rules Triggered
| Rule | Triggered | Blocked |
|------|-----------|---------|
| Brute Force Login | 12 | 8 |
| Failed SSH Attempts | 45 | 0 |
| SQL Injection Attempt | 3 | 3 |
| Port Scan Detected | 8 | 0 |
| Data Exfiltration | 1 | 0 |

### Security Metrics (24h)
- **Total Requests Blocked:** 1,247
- **Unique Attack Patterns:** 15
- **Top Attack Source:** 45.33.22.11 (China)
- **Attack Trend:** +23% vs yesterday

## Recommendations
1. [High] Enable 2FA for all users
2. [High] Block known malicious IPs
3. [Medium] Implement rate limiting on API
4. [Low] Review access logs daily
```
