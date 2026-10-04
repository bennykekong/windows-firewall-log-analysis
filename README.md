# Windows Firewall Log Analysis

**Project completed:** 2025  
**Published to GitHub portfolio:** 2026

## 🔎 Project Overview

This project demonstrates practical Windows Firewall log analysis for identifying suspicious network activity.

The investigation focused on reviewing dropped TCP traffic, identifying a port-scanning attempt, investigating a suspicious single-port connection, and analyzing bad outgoing packets.

---

## 🎯 Project Objectives

- Interpret Windows Firewall log fields
- Analyze dropped TCP packets
- Identify port-scanning activity
- Determine source and destination IP addresses
- Identify scanned destination ports
- Investigate suspicious single-port connections
- Analyze outbound connection attempts
- Use timestamps, packet sizes and ports to correlate suspicious activity
- Document security findings from firewall logs

---

## 🧾 Firewall Log Information

The analyzed Windows Firewall log contained the following header information:

| Field | Value |
|---|---|
| Version | 1.5 |
| Software | Microsoft Windows Firewall |
| Time Format | Local |

---

## 🔍 1. Port Scan Investigation

The firewall logs contained a sequence of dropped packets targeting:

**Destination IP:** `10.0.2.4`

The activity was identified as a port-scanning attempt.

### Findings

| Attribute | Finding |
|---|---|
| First Entry | 2022-12-27 02:32:32 |
| Last Entry | 2022-12-27 02:32:33 |
| Number of Entries | 10 |
| Packet Size | 44 bytes |
| Source IP | 10.0.2.15 |
| Scanned Ports | 21, 80, 135, 139, 445 |

### Security Interpretation

The repeated dropped TCP packets from the same source IP, combined with sequential probing of multiple destination ports, were consistent with port-scanning activity.

---

## 🚨 2. Suspicious Single-Port Connection

A separate sequence of dropped packets targeted a single destination port on:

**Destination IP:** `10.0.2.4`

### Findings

| Attribute | Finding |
|---|---|
| First Entry | 2022-12-27 02:36:53 |
| Last Entry | 2022-12-27 02:37:08 |
| Number of Entries | 8 |
| Packet Size | 52 bytes |
| Source IP | 10.0.2.10 |
| Destination Port | 80 |

### Security Interpretation

Repeated dropped packets from the same source to the same destination port can indicate repeated probing or an attempted connection that requires further investigation.

---

## 📤 3. Suspicious Outgoing Traffic

The investigation also identified dropped outgoing packets originating from:

**Source IP:** `10.0.2.4`

### Findings

| Attribute | Finding |
|---|---|
| First Entry | 2022-12-27 02:39:50 |
| Last Entry | 2022-12-27 02:39:50 |
| Number of Entries | 7 |
| Source Port | 80 |
| Destination Port | 443 |
| Destination IP | 10.0.2.10 |

### Security Interpretation

The repeated dropped outbound connection attempts demonstrated how firewall logs can help identify unusual or unauthorized network communication.

---

## 🛡️ Analysis Techniques

The investigation used several indicators within the Windows Firewall logs:

- DROP actions
- TCP protocol activity
- Source and destination IP addresses
- Source and destination ports
- Packet size
- Timestamps
- Repeated connection attempts
- Direction of network traffic

---

## 🧠 Skills Demonstrated

- Windows Firewall
- Firewall Log Analysis
- Network Security
- SOC Investigation
- Port-Scan Detection
- TCP Traffic Analysis
- Incident Investigation
- Log Correlation
- Network Traffic Monitoring
- Threat Detection
- Security Event Analysis

---

## 📈 Key Takeaways

This project strengthened my ability to analyze firewall logs and identify suspicious patterns within network traffic.

The investigation demonstrated how timestamps, IP addresses, ports, packet sizes and firewall actions can be correlated to identify potentially malicious activity.

---

## 📄 Project Evidence

The completed Windows Firewall Log Analysis submission will be included in this repository as supporting evidence.

---

## 👨‍💻 Author

**Benard Obi Kekong**

Cybersecurity Analyst | CompTIA Security+ | SOC & GRC | Microsoft Sentinel | SIEM | Risk Assessment | Python
