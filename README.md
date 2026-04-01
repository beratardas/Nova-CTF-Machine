# Nova-CTF-Machine
A custom-built vulnerable Linux laboratory designed for offensive security practice, featuring LFI, Log Poisoning, and Privilege Escalation vectors.
# Nova - Boot2Root CTF Machine

![Category](https://img.shields.io/badge/Category-Boot2Root-red)
![Difficulty](https://img.shields.io/badge/Difficulty-Medium%20/%20Hard-orange)
![OS](https://img.shields.io/badge/OS-Linux%20(Ubuntu)-blue)

## Overview
**Nova** is a custom-built, vulnerable Linux penetration testing laboratory designed to simulate real-world attack vectors. This machine was developed to challenge security enthusiasts and practitioners in identifying and exploiting vulnerabilities ranging from web application flaws to internal system misconfigurations. 

The objective is to compromise the machine, navigate through the internal user hierarchy, and ultimately achieve `root` privileges.

## Objectives & Flags
The machine contains **5 hidden flags** that must be captured in order. The environment enforces strict "Least Privilege" principles, meaning flags can only be read by the designated users (e.g., `400` permissions).

1. **Flag 1:** Reconnaissance & Source Code Analysis
2. **Flag 2:** Directory Enumeration
3. **Flag 3:** Initial Access (`www-data` user)
4. **Flag 4:** Lateral Movement (`developer` user)
5. **Flag 5:** Privilege Escalation (`root` user)

## Modeled Attack Vectors (The Kill Chain)
This laboratory requires the attacker to successfully chain multiple vulnerabilities:
* **Web Exploitation:** Local File Inclusion (LFI) leading to Apache Log Poisoning for Remote Code Execution (RCE).
* **Lateral Movement:** Database enumeration, credential harvesting, and MD5 hash cracking to pivot across user accounts.
* **Privilege Escalation:** Exploiting a misconfigured cron job and a custom backup script utilizing a `tar` wildcard injection vulnerability to obtain root access.

## Installation & Setup
1. Download the `.ova` file from the link below.
2. Import the `.ova` file into **VMware Workstation/Player** or **VirtualBox**.
3. Set the Network Adapter to **NAT** or **Bridged** mode.
4. Boot the machine and identify its IP address on your local network using tools like `netdiscover` or `nmap`.

📥 **Download Link:** [Insert MEGA Link Here]

## Author
[cite_start]**Berat Arda Şişko** * Information Security Technology Student [cite: 7] [cite_start]& Cyber Security Club Co-Founder[cite: 8].
* Dedicated to offensive security, digital forensics, and Active Directory exploitation.
* [LinkedIn](https://linkedin.com/in/beratardasisko-92bab3329) | [TryHackMe](https://tryhackme.com/p/beratarda3443) | [HackTheBox](https://profile.hackthebox.com/profile/019d4925-1dbf-722f-829d-678344aecdc6)

## ⚠️ Disclaimer
This virtual machine is intended for educational and authorized testing purposes only. The author is not responsible for any misuse of the techniques demonstrated within this laboratory.
