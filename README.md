# 🏦 Financial-Testbed-IDPS: Intelligent Intrusion Detection & Prevention System

An advanced, intelligent Intrusion Detection and Prevention System (IDPS) engineered to protect a simulated financial infrastructure. This project combines traditional signature-based detection using Snort with proactive Machine Learning-driven mitigation using a Random Forest classifier.

---

## 🏗️ Project Architecture & Experimental Setup

The framework is deployed within a controlled virtual network consisting of two core Linux environments:
1. **Ubuntu Linux (Defense & Monitoring Server):** Hosts the vulnerable banking application, runs Snort IDS, and executes mitigation tasks.
2. **Kali Linux (Attacker Machine):** Used to simulate diverse adversarial tactics and network attacks against the financial testbed.

---

## 🛠️ Current Status & Implementation Roadmap

### ✅ Phase 1: Environment Provisioning & Connection Validation (Completed)
- Successfully deployed two VirtualBox instances: **Kali Linux** (for attacking/auditing) and **Ubuntu Linux** (configured as the target host and monitoring server).
- Performed thorough ICMP connectivity tests to validate the link between both machines.
- <img width="953" height="418" alt="ping result kali to ubuntu" src="https://github.com/user-attachments/assets/3dd0d676-231d-47e0-b9e2-93c4d4164596" />

### ✅ Phase 2: Snort IDS Installation & Configuration (Completed)
- Installed, configured, and deployed **Snort IDS** on the Ubuntu server.
<img width="363" height="136" alt="snort version " src="https://github.com/user-attachments/assets/bab9e27a-0e21-445c-b76d-a17cb37fd4b3" />

### ✅ Phase 3: Custom Snort Rules & Attack Detection (Completed)
- Developed and compiled custom Snort rules that successfully analyze and detect live network threats:
  - **ICMP Custom Rule:** To flag baseline ping scans.
  - **hping Rules:** To capture targeted flooding and custom packet crafts.
  - **Nmap Rules:** To detect active network probing and stealth port scanning.
<img width="434" height="362" alt="nmap ping and dos rules" src="https://github.com/user-attachments/assets/56e7c574-127c-40ba-a2ef-9bc855a23e0e" />

Attack Detection- ICMP

<img width="953" height="418" alt="icmp detection" src="https://github.com/user-attachments/assets/a09323d5-7b5e-41eb-a1d7-48973da683b5" />

Attack Detection -hping

<img width="958" height="467" alt="ddos detection " src="https://github.com/user-attachments/assets/e0c8d779-850b-4c30-a2fc-b84b755ffbbe" />

Attack Detection -nmap

<img width="937" height="352" alt="nmap detection" src="https://github.com/user-attachments/assets/96aa52e3-04c4-4287-a02a-9c6fa9e35634" />

### ✅ Phase 4: Financial Testbed Deployment & Application Hosting (Completed)
- **Hosted and Launched the Website:** Successfully deployed the **Altoro Mutual Banking Website** live on the Ubuntu server. Tested the application to ensure it is fully accessible and working properly as a realistic financial target.
<img width="471" height="293" alt="docker building command" src="https://github.com/user-attachments/assets/145de1e4-3355-4d81-a922-65524d18352f" />

Live website
<img width="953" height="416" alt="altora mutual" src="https://github.com/user-attachments/assets/cee69a31-dfef-48fc-824c-532bd857dcad" />

### ⏳ Phase 5: Real-Time Mobile Alerting via Ntfy (Next Step)
- Integrating the **Ntfy** notification framework to automatically push instant, real-time alert notifications directly to a mobile device the moment Snort detects a critical signature match.

### ⏳ Phase 6: Machine Learning Integration & Automated Prevention (Next Step)
- **Random Forest Algorithm:** Training an ML classifier to analyze live traffic features, filter out false positives, and identify intelligent threat patterns.
- **Automated Mitigation:** Setting up proactive defense responses at the firewall/routing level to block malicious infrastructure dynamically.


