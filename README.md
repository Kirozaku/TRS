<p align="center">
  <img src="https://i.top4top.io/p_3778arqll4.png" width="400">
</p>

<h1 align="center">Tembok Ratapan Solo</h1>

**Tor-based IP Anonymizer Tool**

![Python](https://img.shields.io/badge/Python-3.8+-green?style=flat-square&logo=python)
![Platform](https://img.shields.io/badge/Platform-Kali%20Linux-blue?style=flat-square&logo=linux)
![Tor](https://img.shields.io/badge/Network-Tor-purple?style=flat-square)
![License](https://img.shields.io/badge/License-MIT-yellow?style=flat-square)
![Version](https://img.shields.io/badge/Version-v2.0-brightgreen?style=flat-square)

</div>

---

## 📌 About

**TRS (Tembok Ratapan Solo)** is a Tor-based IP anonymizer tool that runs in the Linux terminal. It allows users to hide their real IP address, switch network identities manually or automatically, and execute commands through the Tor network using Proxychains.

Built for **educational purposes, network security research, and digital privacy**.

---

## ✨ Features

| Feature | Description |
|---|---|
| 🟢 Start / Stop Tor | Manage the Tor service directly from the menu |
| 🔄 Change IP | Request a new Tor circuit for a fresh identity |
| ⏱️ Auto-Rotate IP | Automatically rotate IP at a configurable interval |
| 🔗 Proxychains Exec | Run any command through the Tor network |
| 🔍 DNS Leak Test | Check whether DNS is leaking outside of Tor |
| 📡 Network Info | Display your real IP and Tor IP side by side |
| 🎨 Terminal UI | Matrix rain animation, spinner, progress bar, ASCII art |

---

## ⚙️ Requirements

### System
- OS: **Kali Linux** (or any Debian-based distro)
- Python: **3.8+**
- Privileges: **root / sudo**

### System Packages
```bash
sudo apt update
sudo apt install tor proxychains4 -y
```

### Python Packages
```bash
pip install -r requirements.txt
```

> `requests` and `stem` will be installed automatically. If `stem` is missing when you first change IP, the tool will install it on its own.

---

## 🚀 Installation & Usage

```bash
# 1. Clone the repository
git clone https://github.com/Kirozaku/TRS.git
cd TRS

# 2. Install Python dependencies
pip install -r requirements.txt

# 3. Run the tool (root required)
sudo python3 trs.py
```

---

## 📋 Main Menu

```
[1]  Start Tor
[2]  Stop Tor
[3]  Change IP  (new circuit)
[4]  Auto-Rotate IP
[5]  Execute via Proxychains
[6]  DNS Leak Test
[7]  Show Network Info
[0]  Exit
```

### Auto-Rotate Example
When selecting option `4`, the tool will prompt:
- **Interval** (seconds) — delay between rotations, default `30`
- **Total rotations** — number of rotations, enter `0` for unlimited

### Proxychains Example
When selecting option `5`, enter any command you want to run through Tor, e.g:
```
curl https://ifconfig.me
nmap -sT target.com
```

---

## 🔧 Tor Auto-Configuration

TRS automatically detects and appends the following settings to `/etc/tor/torrc` if they are missing:

```
ControlPort 9051
CookieAuthentication 1
CookieAuthFileGroupReadable 1
```

Tor will then be restarted automatically for the changes to take effect.

---

## 📁 Repository Structure

```
TRS/
├── trs.py              # Main tool file
├── requirements.txt    # Python dependencies
└── README.md           # Documentation
```

---

## ☕ Donate

If you find this tool useful and want to support further development, donations are greatly appreciated!

**Bitcoin (BTC)**
```
1N1rMC95mwYqpQNCWC5TQmZJGdpwf2APsS
```

---

## ⚠️ Disclaimer

> This tool is created **solely for educational and network security research purposes**.  
> Any illegal use of this tool is the **sole responsibility of the user**.  
> The developer is not responsible for any misuse of this tool.

---

## 👤 Author

GitHub: [github.com/Kirozaku](https://github.com/Kirozaku)

---

<div align="center">
  <sub>Stay anonymous. Stay safe.</sub>
</div>
