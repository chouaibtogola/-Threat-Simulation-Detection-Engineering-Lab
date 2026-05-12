# - Pyramid of Pain - Threat-Simulation-Detection-Engineering-Lab
Hands-on cloud security and SOC-style lab covering malware detection, threat simulation, and detection engineering using the Pyramid of Pain and MITRE ATT&amp;CK principles.

# Overview

This project is a purple-team security lab focused on threat simulation, detection engineering, and malware analysis. It was completed as part of a defensive security exercise inspired by real-world incident response scenarios.

The lab simulates an attacker attempting to execute multiple malware samples on an internal workstation, while the defender configures detection mechanisms to identify and stop malicious activity.

# Objective

The main goal of this lab is to strengthen defensive security skills by:

Detecting malware execution in a controlled environment
Applying the Pyramid of Pain model to increase attacker cost
Improving detection engineering capabilities
Understanding how adversaries operate in internal networks
Responding to simulated malware execution events

# Key Concepts Covered
Threat Intelligence & Detection Engineering
Purple Team Operations (Attack + Defense simulation)
Malware detection strategies
MITRE ATT&CK framework mapping
Pyramid of Pain model application
Endpoint monitoring and alerting


# # ----------------  Now here let's start analyzing the sample given using the sandbox  . 

so the bottom level of pyramid of pain highlights hashes . so we are going to look for the hash of the file
we obtain the information below 
<img width="1837" height="601" alt="image" src="https://github.com/user-attachments/assets/7b454587-53ac-4cfb-afa3-97cca823529d" />
now we have few hashes . I am going to use the MD5 hash
<img width="1862" height="614" alt="image" src="https://github.com/user-attachments/assets/d9f51cad-dd14-4be8-a4ff-1a43e3ff63be" />
now I received a confirmation Mail from the purple team that I detected the malware implemented

now the ascending level of pyramid of pain says Ip address

<img width="1860" height="605" alt="image" src="https://github.com/user-attachments/assets/61bca0f7-619c-4b5b-ba5d-fdb719fcf7ac" />

from the sandbox image below , we can see  the ip address we need to block with the firewall 
<img width="1218" height="227" alt="image" src="https://github.com/user-attachments/assets/51cfa489-955b-4099-9b5b-9699c72b94bf" />

now we don't want any egress connection to that IP
<img width="1881" height="600" alt="image" src="https://github.com/user-attachments/assets/faef6571-2eda-49fd-a28a-3b9456623c7d" />

Hooray , we did it agaiin
<img width="1844" height="437" alt="image" src="https://github.com/user-attachments/assets/585c6e4a-0aea-4440-b179-7d737cd1b2cf" />

Now the third bottom pyramid level says domain names. so we will block the domain names from sample 3
<img width="1215" height="242" alt="image" src="https://github.com/user-attachments/assets/75e4a9fa-ccd0-4096-a945-8bc8c800523a" />

now we will no more receive any mail fom this domain
<img width="1875" height="394" alt="image" src="https://github.com/user-attachments/assets/2a8e4de5-56dd-46ef-9a8d-cf7805883bf2" />

