# Wazuh-SIEM-FIM-Automation-Lab
Utilizing a Wazuh Security Information and Event Manager (SIEM) for File Integrity Monitoring (FIM) and Automation to detect and delete malicious files.
## Objective
Within this project I utilized a Wazuh Security Information and Event Manager (SIEM) to automatically remove malware detected on my Ubuntu agent (VM), using Wazuh’s built-in Virustotal integration and active response. Alerts generated were sent to my Wazuh Ubuntu Server, where I was able to monitor the alerts. A simple script was written where once implemented, would delete the malicious file downloaded. This project showcases the importance of monitoring as well as automation to ensure a timely detection and response to malware within a system. 
 

### Skills Learned
- Advanced understanding of SIEM concepts and practical application.
- Enabling and configuring the built-in Wazuh VirusTotal integration on the Wazuh Manager.
- Implementing Active Response, to automatically delete the confirmed malicious file on the Linux agent using a simple bash shell script.
- Ability to generate and recognize attack signatures and patterns.
- Setting up File Integrity Monitoring (FIM) to watch critical directories.
- Development of critical thinking and problem-solving skills in cybersecurity.

### Tools Used
- Wazuh Security Information and Event Management (SIEM) system for log ingestion and analysis.
- Ubuntu Virtual Machines (VMs)
- Virustotal Integration 

## Steps
<img width="1909" height="870" alt="Screenshot 2026-02-09 083131" src="https://github.com/user-attachments/assets/65afdf43-15bb-4105-9bd0-2ba84f4db8c1" />


<img width="1876" height="955" alt="Screenshot 2026-02-09 083159" src="https://github.com/user-attachments/assets/0d790a21-2e10-4a37-a179-484d7446d005" />


Image 1: Setting up the Wazuh Agent from the Wazuh Server. 



<img width="1919" height="1031" alt="Screenshot 2026-02-09 083313" src="https://github.com/user-attachments/assets/90b0070c-c7d2-413e-ba71-3674f27ab9d1" />


Image 2: Confirmation that the Wazuh Agent is showing on the Wazuh Server.


<img width="1907" height="1026" alt="Screenshot 2026-02-09 083829" src="https://github.com/user-attachments/assets/4e174068-8c94-4446-95b0-e5ee19447954" />

Image 3: Confirmation that an alert can be generated from the Wazuh Agent and onto the Wazuh Server. 


<img width="1904" height="992" alt="Screenshot 2026-03-02 171752" src="https://github.com/user-attachments/assets/4ba6aadd-981d-4d8b-aa6f-fcfdd9aa5eac" />

<img width="1911" height="1023" alt="Screenshot 2026-03-02 172813" src="https://github.com/user-attachments/assets/fbd79fc7-2fcf-437a-b5ac-0105c8dd6a53" />


Image 4: Configuring agent.conf (Wazuh Server) to generate alerts on the agent for FIM. 


<img width="1895" height="1024" alt="Screenshot 2026-03-02 172916" src="https://github.com/user-attachments/assets/abe52c0c-bf0d-4266-98bc-92822e47daf6" />

Image 5: Confirmation that an added file will generate an alert. 


<img width="1909" height="1026" alt="Screenshot 2026-03-16 110807" src="https://github.com/user-attachments/assets/6a20d20f-0332-435c-ad92-5e85bbaee326" />

Image 6: Testing the Virustotal Integration via terminal on the Wazuh Agent "sudo curl -Lo /media/user/software/suspicious-file.exe https://secure.eicar.org/eicar.com"
  - Virustotal Integration steps can be found here: https://documentation.wazuh.com/current/user-manual/capabilities/malware-detection/virus-total-integration.html



<img width="1906" height="1030" alt="Screenshot 2026-03-16 111040" src="https://github.com/user-attachments/assets/1b486863-10e0-45d7-b79c-cbd5ddf34db0" />


<img width="1913" height="1026" alt="Screenshot 2026-03-16 111518" src="https://github.com/user-attachments/assets/a7f20860-38cd-486e-b5eb-a6d1e280c4b8" />


<img width="1540" height="993" alt="Screenshot 2026-03-16 111534" src="https://github.com/user-attachments/assets/443469c5-db7e-46c0-93b0-0abe5418c059" />


Image 7: Confirmation that the Virustotal Integration is working, an alert was generated including details with various hashes (MD5,Sha1). A link was provided in the details linking to further information on the malware via Virustotal. 

<img width="1185" height="681" alt="Screenshot 2026-03-16 113344" src="https://github.com/user-attachments/assets/18a7813e-dac4-4cf7-bd66-fcb4bd1c466b" />


<img width="1906" height="1028" alt="Screenshot 2026-03-16 113800" src="https://github.com/user-attachments/assets/2c232b8d-01c8-4f64-9707-9f0f50b63bcc" />




Image 8: Detecing and removing malware using VirusTotal Integration
  - On the Wazuh Agent
  - https://documentation.wazuh.com/current/proof-of-concept-guide/detect-remove-malware-virustotal.html


<img width="1919" height="558" alt="Screenshot 2026-03-16 112109" src="https://github.com/user-attachments/assets/2cc7087c-373e-46ff-9f8c-bee59135050b" />



<img width="951" height="1030" alt="Screenshot 2026-03-16 122205" src="https://github.com/user-attachments/assets/374ff252-dbe8-4e78-8483-f9a0d6166092" />


Image 9: Configuring the Wazuh Server 
  - Perform the following steps on the Wazuh server to alert for changes in the endpoint directory and enable the VirusTotal integration. These steps also enable and trigger the active response script whenever a suspicious file is detected.
  - https://documentation.wazuh.com/current/proof-of-concept-guide/detect-remove-malware-virustotal.html


<img width="1917" height="1023" alt="Screenshot 2026-03-16 121938" src="https://github.com/user-attachments/assets/c6f81f8b-5765-4b20-a16e-10843390b01f" />

<img width="1909" height="1013" alt="Screenshot 2026-03-16 121946" src="https://github.com/user-attachments/assets/f1535451-3ba4-4472-8eaf-4bb6399e68e2" />


Image 10: Attack emulation, response and deletion by automation. 
  - Download the EICAR test file once again and watch as the automation works and deletes the file.


<img width="1906" height="1031" alt="Screenshot 2026-03-16 122112" src="https://github.com/user-attachments/assets/26325bac-09b5-4feb-ae74-9579e14dcc02" />

Image 11: An alert is still generated on the Wazuh SIEM. The timeline shows the EICAR file being downloaded, an alert is generated, and then deleted all via the automation and integration set up. 





