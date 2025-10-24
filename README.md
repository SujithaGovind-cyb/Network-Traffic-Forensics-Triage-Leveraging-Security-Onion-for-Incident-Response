# Network Traffic Forensics Triage Leveraging Security Onion for Incident Response

This project showcases a complete network traffic investigation using Security Onion's integrated suite of tools (Kibana, Wireshark, Hunt). The core objective was to analyze a captured PCAP file to perform alert triage, prioritize suspicious events, create detailed incident cases, and conduct deep packet inspection to identify malicious activity. This exercise demonstrates proficiency in Security Operations Center (SOC) processes, specifically the ability to move from high-level alerts to detailed forensic evidence, addressing threats like potential intrusion attempts and malware activity.

### Skills Learned

Network Traffic Analysis (NTA) 
- Expertise in examining packet capture (PCAP) data to identify anomalous or malicious traffic patterns.

Alert Triage & Prioritization 
- Using Security Onion's dashboard and filtering capabilities to manage high-volume alerts and escalate high-severity incidents.

SOC Case Management 
- Creating, enriching, and managing incident cases for documented response and remediation.

PCAP Deep Dive 
- Utilizing Wireshark for granular analysis of individual packets, headers, and payloads to confirm the nature of an attack (e.g., HTTP POST requests, IP communication).

Threat Hunting (OQL) 
- Applying the Hunt Module with custom Open Query Language (OQL) queries to aggregate and analyze network data related to specific threats or indicators of compromise (IOCs).

### Tools Used

- Network Security Monitoring (NSM) Platform: Security Onion (including Kibana, Squert, TheHive)
- Packet Analyzer: Wireshark (for deep inspection)
- Threat Hunting Language: Open Query Language (OQL)
- Data Visualization: Kibana

## Steps

The investigation followed a structured, playbook-driven approach, mirroring real-world SOC processes:

1. PCAP Ingestion and Initial Alert Review

- File Upload: Successfully ingested the target PCAP file into the Security Onion platform for automated analysis and alert generation.
- Dashboard Triage: Navigated the main dashboard to review network metrics and initially prioritize alerts based on severity, ensuring focus on critical threats first.
- Alert Filtering: Applied filters and sorting criteria to focus on specific suspicious activities, such as potential intrusion attempts and potential malware activity.

2. Alert Escalation and Case Management

- Suspicious Activity Identification: Identified a high-priority, recurring alert—specifically the "ET HUNTING GENERIC SUSPICIOUS POST to Dotted Quad with Fake Browser"—due to its repetitive nature and target ports.
- Case Creation: Escalated the specific suspicious alert into a formal incident Case within Security Onion's management module.
- Case Enrichment: Documented observations, added relevant screenshots, and enriched the case with initial findings (e.g., target IPs, associated ports) to support detailed investigation.

3. Deep Packet Inspection (Wireshark)

- PCAP Extraction: Extracted the relevant PCAP data associated with the escalated case for granular analysis.
- Protocol Analysis: Used Wireshark to examine the communication flow, focusing on the contents of the suspicious HTTP POST requests.
- Payload Examination: Confirmed the contents of the POST requests and identified the target malicious IP addresses, providing clear evidence of the suspicious endpoint interaction and potential data transfer.

4. Threat Hunting and Final Analysis

- OQL Query Execution: Leveraged the Hunt module and OQL queries to aggregate and analyze all related network traffic information (e.g., repeated intrusion attempts, volume of data transferred to suspicious IPs).
- Endpoint Correlation: Utilized endpoint analysis insights (from Security Onion's components) to further flag the suspicious POST requests and interaction with fake browsers, confirming the nature and scope of the threat.
- Mitigation Summary: Summarized the findings, detailing the unusual activity and traffic patterns detected, and provided an actionable conclusion for incident mitigation and proactive defense enhancement.

Ref 1: Security Onion Case Events
