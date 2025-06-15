# 🔐 Wazuh SSH Brute-force Detection Lab

A virtualized lab that demonstrates real-time detection of SSH brute-force attacks using **Wazuh SIEM** and **Hydra**. This project simulates a real-world intrusion and shows how Wazuh identifies and classifies the attack using MITRE ATT&CK techniques.

## 🧠 Overview

This lab simulates a basic blue team setup:

- **Wazuh Manager** for centralized security event monitoring  
- **Wazuh Agent** on the Ubuntu target to collect logs  
- **Kali Linux** using Hydra to perform SSH brute-force attacks  
- MITRE ATT&CK mappings automatically applied to alerts  

## 🖼️ Architecture Diagram


- All systems run in a **VirtualBox NAT network**
- SSH is exposed on Ubuntu Target (default port 22)

## 🧪 Attack Simulation

### 🔧 Tool Used: [Hydra](https://github.com/vanhauser-thc/thc-hydra)

Run this from your **Kali Linux** machine:

```bash
hydra -l james -P /usr/share/wordlists/rockyou.txt ssh://10.0.2.4

```
![wazuh-ssh](https://github.com/user-attachments/assets/569b7824-2ed4-4be7-8ff9-90bd294b324d)
