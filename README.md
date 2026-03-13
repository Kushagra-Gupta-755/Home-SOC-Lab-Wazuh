# Home SOC Lab using Wazuh SIEM

## Project Overview

This project demonstrates a **Home Security Operations Center (SOC) Lab** built using the **Wazuh SIEM platform**. The lab simulates a monitored network environment where endpoint logs are collected, analyzed, and used to detect suspicious activity.

The goal of this project is to gain experience with **SIEM deployment, endpoint monitoring, log analysis, threat detection, and security event investigation** in a virtual environment.

---

## Key Features

- SIEM deployment using **Wazuh**
- Endpoint monitoring using **Wazuh Agent**
- **File Integrity Monitoring (FIM)** to detect file changes
- **Windows Security log monitoring**
- **PowerShell activity monitoring**
- **Firewall log monitoring & network scan detection**
- **Vulnerability detection** using Wazuh’s vulnerability module
- **Threat hunting and security event investigation**

---

## Lab Architecture

The lab environment consists of three virtual machines running inside a virtual network.

| Machine | Role |
|--------|------|
| Kali Linux | Attacker machine used for attack simulation |
| Windows 11 | Monitored endpoint running Wazuh Agent |
| Ubuntu Server | Wazuh SIEM server |

    +---------------------+
    |     Kali Linux      |
    |   Attacker Machine  |
    |     (Nmap Scan)     |
    +----------+----------+
               |
               | Attack Traffic
               v
    +---------------------+
    |     Windows 11      |
    |      Endpoint       |
    |     Wazuh Agent     |
    +----------+----------+
               |
               | Security Logs
               v
    +---------------------+
    |      Ubuntu VM      |
    |     Wazuh Server    |
    |  Manager + Indexer  |
    |     Dashboard       |
    +---------------------+
               |
               v
        SOC Monitoring
           Dashboard


---

## SOC Detection Workflow


Attack Simulation (Kali Linux) → Endpoint Activity (Windows 11) → Log Collection (Wazuh Agent) → Log Analysis (Wazuh SIEM) → Security Alerts (Wazuh Dashboard) → Threat Investigation


---

## Technologies Used

- **Wazuh SIEM**
- **VMware Workstation**
- **Ubuntu Server**
- **Windows 11**
- **Kali Linux**
- **Nmap**

---

## Author

**Kushagra Gupta**
