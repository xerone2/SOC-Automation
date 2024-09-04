## SOC Automation

### Overview
This project implements a comprehensive Security Orchestration, Automation, and Response (SOAR) solution, designed to streamline and automate security operations. By integrating a suite of tools, including Wazuh, TheHive, Shuffle, and Sysmon, the system provides efficient threat detection, incident response, and investigation capabilities.

### Tools Used
* **Wazuh:** An open-source security monitoring solution that provides real-time alerting, intrusion detection, and log analysis.
* **DigitalOcean:** A cloud computing platform used to host the Wazuh manager and TheHive.
* **TheHive:** A security incident response platform that allows for efficient incident management, investigation, and reporting.
* **Shuffle:** A tool designed to enrich Indicators of Compromise (IOCs) using OSINT sources and trigger appropriate actions based on predefined rules.
* **Sysmon:** A system monitoring tool that provides detailed information about system processes, network connections, and file activity.




![Automation Workflow](https://github.com/xerone2/SOC-Automation/blob/main/Automation-Diagram.png)





### Workflow
1. **Event Collection:** The Wazuh agent on the Windows 10 client collects security-related events and forwards them to the Wazuh manager.
2. **Alert Generation:** The Wazuh manager analyzes the incoming events and generates alerts based on predefined rules and signatures.
3. **IOC Enrichment:** The Shuffle component enriches the IOCs associated with the alerts using OSINT sources like VirusTotal.
4. **Alert Distribution:** The Shuffle sends the enriched alerts to TheHive for incident management.
5. **Incident Investigation:** Security analysts in TheHive can investigate the incidents, gather additional evidence, and take appropriate response actions.
6. **Notification:** The Shuffle can also send notifications to SOC analysts via email or other communication channels.

### Installation and Configuration
* [**Wazuh**](https://github.com/xerone2/SOC-Automation/blob/main/Wazuh-Installation.md)
* [**TheHive**](https://github.com/xerone2/SOC-Automation/blob/main/TheHive-Installation.md)
* [**Sysmon**](https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqbU5Zak9XZ29HN3JqT1pTY29KdTI1b3pnakhtQXxBQ3Jtc0ttTXlzNlZmdWtBTkdRUlNhb0g3SEtSdUFNNy05ZlEzNE1FNVFHQ0NnZC1TWEEtdEphcFZ6UG9QRGtudUd5bjl2aTFzWV9SVGo3dWMzY2h2QmpVU2loTDBqdmwydXJTUnFpTW5sQUJtd213LUxVY1NXbw&q=https%3A%2F%2Flearn.microsoft.com%2Fen-us%2Fsysinternals%2Fdownloads%2Fsysmon&v=uJ7pv6blyog)
* [**Shuffle**](https://shuffler.io/)

### Additional Considerations
* **Rule Creation:** Develop and maintain effective Wazuh rules to detect a wide range of security threats.
* **Playbook Development:** Create playbooks in TheHive to automate incident response workflows and streamline investigations.
* **Integration with Other Tools:** Consider integrating the system with other security tools like SIEMs, EDR solutions, and SOAR platforms.
* **Continuous Monitoring and Improvement:** Regularly monitor the system's performance and make necessary adjustments to ensure optimal security posture.
