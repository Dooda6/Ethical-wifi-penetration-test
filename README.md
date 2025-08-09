# Ethical Wi-Fi Penetration Testing Demo

## 📜 Project Overview
This project demonstrates an **authorized Wi-Fi penetration test** conducted in a controlled lab environment.  
The objective was to capture WPA/WPA2 handshake packets and attempt password recovery to evaluate wireless security.

> **Disclaimer:**  
> All testing was performed on my **own network** and/or with explicit written permission from the network owner.  
> Unauthorized access to networks is illegal and punishable by law.

---

## 🛠 Tools Used
- **Airodump-ng** – Captures WPA/WPA2 handshakes.
- **Wireshark** – Analyzes network packets, verifies handshake capture.
- **Aircrack-ng** – Performs dictionary-based password cracking.
- **Hashcat** – GPU-accelerated password cracking.

---

## 🔍 Process

### 1️⃣ Capturing the Handshake
```bash
airodump-ng -w wificapture -c 11 --bssid wlan0mon

