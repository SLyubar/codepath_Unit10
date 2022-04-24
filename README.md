# Honeypot Assignment

**Time spent:** **10** hours spent in total

**Objective:** Create a honeynet using MHN-Admin. Present your findings as if you were requested to give a brief report of the current state of Internet security. Assume that your audience is a current employer who is questioning why the company should allocate anymore resources to the IT security team.

### MHN-Admin Deployment (Required)

**Summary:** How did you deploy it? Did you use GCP, AWS, Azure, Vagrant, VirtualBox, etc.?

I deployed this project using Google Cloud Platform (GCP). I created an account with free credits and then created an MHN-Admin Virtual Machine (VM) instance. I applied the required firewall rules to it and then connected to a secure shell (SSH). I did not download the Google Cloud SDK. Instead, I did all my steps within the Cloud Shell provided on the GCP website inside the browser. After installing the required MHN applications and dependencies, I was able to open the MHN-Admin portal through the browser using MHN-Admin's external IP created by GCP. Next, I created a Honeypot the below honeypot VM instance and attacked using NMAP in my Kali machine. Finally, I downloaded the attacks to a session.json file.

<img src="https://github.com/SLyubar/codepath_Unit10/blob/main/MHN_Admin_Deploy.gif">

### Dionaea Honeypot Deployment (Required)

**Summary:** Briefly in your own words, what does dionaea do?

Dionaea is an insecure server that can be accessed by external port scanners and other malware. Its purpose is to trick predominantly malicious actors into attacking it and then capturing their identifying information such as their geolocation, IP address, and hopefully malware signatures. This can help security researchers determine the type of threats that are in the wild. It may even help law enforcement gather evidence to arrest or shut down malicious actors.

<img src="https://github.com/SLyubar/codepath_Unit10/blob/main/Honeypot_Deploy.gif">

### Database Backup (Required) 

**Summary:** What is the RDBMS that MHN-Admin uses? What information does the exported JSON file record?

MHN-Admin used a NoSQL database called MongoDB that stores data in JSON documents instead of rows and tables. The exported JSON file records key-value pairs with attack data such as the protocol being used, timestamp of the attack, source IP, source port, destination port, and type of honeypot used.

*Be sure to upload session.json directly to this GitHub repo/branch in order to get full credit.*

<img src="https://github.com/SLyubar/codepath_Unit10/blob/main/Attack_Database.gif">

## Notes

I have never used Google Cloud Platform before so initial setup and understanding the commands, regions, etc. was a challenge. Once, I was able to get everything working, I had to redo the assignment to capture GIFs. Some steps were very long so it was challenging to record everything without it being exceedingly long. I spent a while trimming the GIFs so it would be a more manageable length.
