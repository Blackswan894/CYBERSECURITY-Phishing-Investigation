# CYBERSECURITY-Phishing-Investigation
Wireshark-based phishing investigation showcasing packet analysis, IoC detection, and incident response documentation.

 Phishing & Packet Capture Investigation  
By: Tochi Ndukwe  
In this project, I investigated a phishing incident using Wireshark to analyze packet capture (PCAP) data. 

In this project, I analyzed a .pcap file to detect phishing emails using Wireshark. To efficiently identify malicious activity, I applied several SMTP display filters to isolate suspicious traffic.

The investigation revealed that the source IP address 10.6.1.104 was repeatedly involved in sending phishing emails. Using filters such as smtp.req.command == "MAIL" and smtp.response.code == 250, I identified the sender and recipients of these emails. I also examined smtp.data.fragments to reconstruct fragmented SMTP data, which helped reveal hidden payloads and malicious content.

Further analysis of the SMTP headers showed signs of phishing, including spoofed sender addresses, unusual attachments, and links crafted to steal user credentials. To validate my findings, I referenced the Wireshark Display Filter Reference for SMTP and refined my filters accordingly. Finally, using the command ip.addr == 10.6.1.104, I confirmed that this IP address was indeed the source of the attack.

This project strengthened my skills in packet analysis, network forensics, and identifying phishing indicators within captured network traffic.
  
This hands-on investigation simulated a Security Operations Center (SOC) scenario, where defenders must analyze suspicious traffic and respond effectively.

Tools & Technologies  
- **Wireshark** – Packet capture and SMTP traffic analysis  
- **PCAP Analysis** – Filtering and reconstructing SMTP sessions  
- **Incident Response Documentation** – Reporting and recommendations  






