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

> airodump-ng -w wificapture -c --bssid  wlan0mon

---

### 2️⃣ Verifying the Handshake with Wireshark
- ** Loaded the .cap file into Wireshark.
- ** Filtered for eapol frames.
- ** Confirmed the presence of the 4-way handshake.
---
### 3️⃣ Cracking the Password

> aircrack-ng wificapture-01.cap -w /usr/share/wordlists/rockyou.txt

> hashcat -m 22000 wificapture-01.hc22000 /usr/share/wordlists/rockyou.txt

---
### 📚 Key Learning Points
Setting a Wi-Fi adapter to monitor mode for packet capture.

Capturing WPA/WPA2 4-way handshake packets.

Using EAPOL packet inspection to confirm capture success.

Performing dictionary attacks and understanding password complexity.

Importance of strong passphrases to prevent brute-force attacks.



