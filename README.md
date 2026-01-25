# Android OPSEC Guide

This repository provides a straightforward guide to enhancing operational security (OPSEC) and cybersecurity on Android devices. It focuses on protecting against phishing, malware, IP tracking, data mining and device fingerprinting using free, open source tools. This method acts as a proxy like setup for privacy conscious browsing and app usage, ideal for users new to cybersecurity who may currently rely on paid VPNs, Cloudflare or Google DNS.

**Note:** This guide is for Android 10 or later. It emphasizes privacy without requiring root access.

## Requirements
- Android device running version 10 or above.
- **DuckDuckGo App Browser:** Download from [https://duckduckgo.com/app](https://duckduckgo.com/app).
- **Orbot App:** Download from [https://github.com/guardianproject/orbot-android/releases/tag/17.8.0-RC-1-tor-0.4.8.21](https://github.com/guardianproject/orbot-android/releases/tag/17.8.0-RC-1-tor-0.4.8.21).
- **Tuta Mail App:** Download from [https://f-droid.org/repo/de.tutao.tutanota_396578.apk](https://f-droid.org/repo/de.tutao.tutanota_396578.apk).
- **Fake Traveler App:** Download from [https://f-droid.org/repo/cl.coders.faketraveler_222.apk](https://f-droid.org/repo/cl.coders.faketraveler_222.apk).
**Recommendation:** Avoid downloading from the Google Play Store to minimize tracking. Use F-Droid or direct APK links instead.
## Setup Instructions
Follow these steps in order to configure your device for improved privacy and security.
### Step 1: Configure DNS and MAC Randomization
1. Go to **Settings > Network & Internet > Private DNS**.
2. Select **Private DNS provider hostname** and enter `dns.quad9.net`. Save the changes.
3. Go back to **Network & Internet > Internet**, select your network, then tap **Network usage** and set it to **Treat as unmetered**.
4. In the same menu, go to **Privacy** and enable **Use randomized MAC**. Disable **Send device name**.
### What this does:  
Quad9 DNS blocks malicious domains, protects against malware and phishing, and does not log or collect user data (unlike Google or Cloudflare DNS). For more details, visit [https://www.quad9.net/](https://www.quad9.net/).  
Setting the network as unmetered reduces monitoring. Randomized MAC changes your device's hardware identifier on networks, preventing tracking (e.g., it might appear as a random device like a fridge).
### Step 2: Enable DuckDuckGo App Tracking Protection
1. Open the DuckDuckGo app and complete the initial setup (recommended as your primary browser for zero trackers).
2. Tap the three dots menu > **App Tracking Protection** > Enable.
3. Go to **Settings > Network & Internet > VPN** and enable **Always-on VPN** for DuckDuckGo.
### What this does:
Blocks hidden trackers in apps that steal data for targeted ads or phishing. DuckDuckGo ensures private browsing without third party tracking.
### Step 3: Configure Orbot for Tor Connectivity
1. Open Orbot and allow notifications. **Do not connect yet** (to avoid conflicts with DNS and DuckDuckGo).
2. Tap **More > Settings**.
3. Enable **Power user mode** (prevents VPN mode).
4. Scroll to **Connectivity** and enable all **Isolate** options (e.g., Isolate destination addresses).
5. Go back, select **Choose how to connect > Direct connection to Tor**, then connect.
### What this does:
It encrypts traffic and obscures your online fingerprint using the Tor network. Isolation ensures apps route through separate circuits for better privacy.
### Step 4: Set Up Secure Email with Tuta
1. Open Tuta Mail and create an account (recommend using a `.de` domain for German privacy laws).
2. For added security, link a temporary DuckDuckGo email alias to your Tuta account and use aliases for sign ups.
### What this does:
Tuta provides end-to-end encrypted email with zero trackers, ads, or data mining. It spoofs locations and protects metadata preventing phishing or doxxing via email headers.
### Step 5: Spoof Location with Fake Traveler
1. Open Fake Traveler, select a location on the map, and apply it.
2. Go to **Settings > About phone** and tap **Build number** seven times to enable Developer options.
3. In **Developer options**, scroll to **Select mock location app** and choose Fake Traveler.
4. While in Developer options, enable **Non-persistent MAC** (complements randomization) and **Tethering hardware acceleration**.
### What this does:
Spoofs your device's geolocation, preventing apps from determining your real position.
## Final Checks and Tips
- Ensure App Tracking Protection is **off** for Orbot to avoid conflicts.
- Allow background network and battery usage for DuckDuckGo and Orbot.
- Prefer Wi-Fi over mobile data for better performance.
- You should notice faster internet speeds and stronger privacy. If stuck contact us via our website: https://dresoperatingsystems.github.io/.

After setup, your device will have hardened cybersecurity reducing risks from online threats.
---
**Thank you for using this guide.**     
**The DresOS Team**  
