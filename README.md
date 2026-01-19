# MikroTik ISP Setup - OUR BANK LTD

This project is a simulation of how an ISP or a large office network can be managed using **MikroTik RouterOS**. I’ve configured this specifically for **OUR BANK LTD** to ensure the internet is distributed fairly and securely among users.

### 🛠 What’s inside this setup?

* **PPPoE Server:** Instead of a simple Wi-Fi password, I used a PPPoE server. This means every user needs their own ID and password to get online. For security, I disabled the old "PAP" method so passwords aren't sent in plain text.
* **Smart Bandwidth (PCQ):** We’ve all been on networks where one person downloading a movie slows it down for everyone. I fixed that using **PCQ (Per Connection Queuing)**. It automatically limits every user to a steady **10 Mbps**, so the connection stays smooth for everyone.
* **Network Security:** * **NAT/Masquerade:** Configured to let local users browse the web safely.
    * **One Session Policy:** I’ve restricted it so one account can only be logged in from one device at a time—no account sharing!
* **Full Connectivity:** I’ve tested the routing with Google DNS (8.8.8.8), and the pings are stable with 0% packet loss.

### 📁 Files in this Repo
* `MIKROTIK PROJECT Documentation.pdf`: A step-by-step guide with screenshots of the whole process.
* `auto-before-reset.backup`: The actual MikroTik backup file. You can restore this on your own router to see the settings live.

### 🚀 How to use it
If you have MikroTik RouterOS (or a virtual one in GNS3/EVE-NG), you can simply load the backup file. The WAN is set to `ether1` and the users connect via `ether2`.

**Project by:** SYED BAIJID 
