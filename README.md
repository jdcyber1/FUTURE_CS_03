# FUTURE_CS_03
Internship Report:3.Wi-Fi Security Assessment of Home Network

1. Introduction
This task involved conducting a Wi-Fi security assessment on my personal home network to evaluate its resilience against unauthorized access and other vulnerabilities.
 The goal was to identify weak points and recommend security improvements.

2. Tools Used
Wireshark – For monitoring network traffic.


Aircrack-ng – For assessing Wi-Fi password strength and encryption standards.


Nmap – For scanning open ports and detecting connected devices.



3. Methodology
3.1 Wi-Fi Traffic Analysis (Wireshark)
Opened Wireshark.


Selected the wireless network interface.


Captured wireless packets to inspect any unencrypted traffic.


Checked for suspicious activity or unauthorized data transmission.




3.2 Password and Encryption Testing (Aircrack-ng)
Used Airmon-ng to enable monitor mode:

sudo airmon-ng start wlan0
Captured handshake packets using:
sudo airodump-ng wlan0mon
Attempted to analyze WPA2 encryption and test password strength with a wordlist.






3.3 Network Scanning (Nmap)
Scanned the home network to detect active devices and open ports:
sudo nmap -sn 192.168.0.1/24
dentified all connected devices (phones, laptops, TVs, etc.)
Conducted a basic TCP port scan on the router:
sudo nmap -p- 192.168.0.1


4. Observations
Category
Observations
Wi-Fi Encryption
WPA2-Personal (AES)
Password Strength
Good (12+ characters, special symbols)
Unauthorized Devices
No unauthorized devices found
Open Ports on Router
Ports 80 (HTTP) and 443 (HTTPS) open
Traffic Monitoring
No unencrypted sensitive information detected


5. Vulnerabilities Identified
Default Router Login Credentials were not changed.


HTTP management access to router (unsecured web access).


No VPN used for added encryption.



6. Recommendations
Change router admin credentials from default to a strong, unique password.


Disable remote management over HTTP; use HTTPS only if needed.


Enable MAC address filtering to restrict access to known devices.


Regular firmware updates for the router to patch vulnerabilities.


Use a VPN for extra security while accessing the internet.


