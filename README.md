# WiFi Penetration Testing Lab: WPA2 Handshake Capture & Cracking

## ⚠️ Legal & Ethical Disclaimer
**This project was conducted exclusively on my own private network and devices for educational purposes only.** The goal is to understand WiFi security vulnerabilities to better defend against them. Unauthorized access to networks or devices is illegal and unethical. Always obtain proper authorization before testing.

---

## 🎯 Project Objectives
- Set up a controlled lab environment with Kali Linux.
- Capture a WPA2 4-way handshake from my own router.
- Attempt to crack the password using a dictionary attack with `rockyou.txt`.
- Understand the mechanics of deauthentication attacks and dictionary-based cracking.

---

## 🛠️ Prerequisites & Tools

### Hardware
- Laptop with Kali Linux (or VM with USB passthrough).
- External WiFi adapter supporting monitor mode and packet injection (e.g., ALFA AWUS036ACH).
- Target router: FRITZ!Box 6660 Cable RX (my own).

### Software
- `aircrack-ng` suite (includes `airmon-ng`, `airodump-ng`, `aireplay-ng`, `aircrack-ng`).
- Wordlist: `rockyou.txt` (from `/usr/share/wordlists/`).

---

## 📝 Step-by-Step Methodology

### 1. Enable Monitor Mode
```bash
sudo airmon-ng check kill
sudo airmon-ng start wlan0
