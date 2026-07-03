# 🛡️Brute-force-attack-analysis-lab
## 🧠 Objective
- Perform SSH and FTP brute force attacks in a lab environment
- Generate authentication failure logs on Ubuntu
- Forward logs to Wazuh SIEM
- Detect brute force patterns using Wazuh alerts
- Understand SOC monitoring workflow

---

## 🖥️ Lab Environment

| Component | Details |
|-----------|---------|
| Attacker Machine | Kali Linux |
| Target Machine | Ubuntu Server |
| SIEM Tool | Wazuh |
| Services Tested | SSH, FTP |
| Network | VirtualBox / VMware Internal Network |

---

## ⚙️ Tools Used

![Kali](https://img.shields.io/badge/Kali%20Linux-557C94?style=for-the-badge&logo=kalilinux&logoColor=white)
![Ubuntu](https://img.shields.io/badge/Ubuntu-E95420?style=for-the-badge&logo=ubuntu&logoColor=white)
![Wazuh](https://img.shields.io/badge/Wazuh-SIEM-blue?style=for-the-badge)
![Hydra](https://img.shields.io/badge/THC--Hydra-Brute%20Force-red?style=for-the-badge)
![SSH](https://img.shields.io/badge/SSH-Secure_Shell-black?style=for-the-badge&logo=openssh&logoColor=white)
![FTP](https://img.shields.io/badge/FTP-File_Transfer-orange?style=for-the-badge)
![Kibana](https://img.shields.io/badge/Kibana-Dashboard-005571?style=for-the-badge&logo=kibana&logoColor=white)
---

## 🚀 Attack Simulation
# 🔐 SSH & FTP Brute Force Attack Lab using Wazuh

## 🔹 SSH Brute Force Attack

hydra -l ubuntu -P rockyou.txt ssh://<target-ip>

📸 Screenshot:  
![SSH Brute Force](screenshots/sshbf.png)

---

## 🔹 FTP Brute Force Attack

hydra -l ftpuser -P rockyou.txt ftp://<target-ip>

📸 Screenshot:  
![FTP Brute Force](screenshots/ftpbf.png)

---

## 📡 Log Collection (Ubuntu → Wazuh)

Collected logs:
- /var/log/auth.log
- /var/log/vsftpd.log

📸 Screenshot:  
![Log Collection Dashboard](screenshots/ftpdash.png)

---

## 🧾 Wazuh Detection Results

- Multiple failed login attempts detected  
- Brute force alert triggered  
- Source IP marked suspicious  
- Events visible in Wazuh dashboard  

📸 Screenshot:  
![Attack Dashboard](screenshots/attack-dboard.png)

---

## 📊 Key Findings

- SSH brute force is easily detectable via auth.log  
- FTP logs require careful parsing but still detectable  
- Wazuh rules successfully detect repeated failed logins  
- Threshold-based alerts work effectively  

---

## 🧠 Learning Outcome

- Understanding brute force attack behavior  
- Working with SIEM (Wazuh)  
- Log analysis and threat detection  
- SOC workflow exposure  

---


## ⚠️ Disclaimer
This project is strictly for educational purposes in a controlled lab environment. Unauthorized access to systems is illegal.

