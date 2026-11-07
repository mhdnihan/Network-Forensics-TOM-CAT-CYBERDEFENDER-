# Network-Forensics-TOM-CAT-CYBERDEFENDER-


PCAP-Based Network Forensics:  Investigation

#Project Overview

Performed a network traffic investigation using Wireshark to analyze a PCAP file from a simulated Apache Tomcat server compromise scenario on CyberDefenders.

The objective was to identify the source of suspicious network activity, investigate web server access, identify the attacker’s enumeration techniques, and trace the malicious activity leading to a reverse shell connection.

#Investigation Methodology

1. Network Traffic Analysis

* Analyzed network conversations using Wireshark’s Statistics → Conversations feature.
* Identified suspicious IP addresses based on network traffic volume and communication patterns.
* Investigated the source IP responsible for scanning multiple ports across the network.

2. Attacker IP Geolocation

* Used external IP intelligence and geolocation tools to investigate the identified source IP.
* Identified China as the geolocation associated with the IP address.

3. Web Server Access Investigation

* Filtered HTTP traffic associated with the suspicious source IP.
* Analyzed HTTP requests to identify accessible web services and administrative interfaces.
* Identified port 8080 as the web server port involved in the suspicious activity.

4. Attacker Tool Identification

* Used Wireshark’s Follow → TCP Stream feature to reconstruct TCP communication.
* Examined HTTP requests and responses to identify the tools and techniques used by the attacker.
* Observed enumeration attempts against multiple administrative panels.
* Identified the administrative interface that returned a successful response.

5. Authentication Analysis

* Applied the Wireshark display filter http.authbasic to investigate HTTP Basic Authentication traffic.
* Examined authentication requests and identified the credentials used during the attack.
* Analyzed session-related information present in the HTTP traffic.

6. Malicious Payload Analysis

* Reconstructed TCP streams to inspect the files submitted to the server.
* Identified the successfully submitted file and examined its contents.
* Discovered reverse shell code embedded in the submitted payload.
* Extracted the attacker’s IP address and destination port associated with the reverse shell communication.

Tools & Techniques

* Wireshark – Packet capture analysis and TCP stream reconstruction.
* IP Geolocation Tools – Source IP investigation.
* HTTP Analysis – Request, response and authentication inspection.
* TCP Stream Analysis – Communication reconstruction and payload investigation.
* Wireshark Display Filters – Traffic filtering and investigation.

Key Findings

* Identified the suspicious source IP responsible for network scanning.
* Determined the geolocation associated with the source IP.
* Identified the web server service running on port 8080.
* Discovered administrative panel enumeration attempts.
* Identified authentication credentials exposed in HTTP traffic.
* Reconstructed the submitted malicious file.
* Identified reverse shell code and its associated attacker IP and port.

Learning Outcomes

* Practical experience in PCAP-based network forensics.
* Understanding TCP conversations and stream reconstruction.
* Identifying network reconnaissance and web server enumeration.
* Analyzing HTTP authentication mechanisms.
* Investigating malicious file uploads and reverse shell activity.
* Developing a structured network incident investigation workflow.

Lab Platform: CyberDefenders
Lab Scenario: Tomcat Takeover
Primary Tool: Wireshark
Category: Network Forensics | Incident Investigation | Threat Analysis
