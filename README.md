## SOC Automation

### Overview
This project implements a comprehensive Security Orchestration, Automation, and Response (SOAR) solution, designed to streamline and automate security operations. By integrating a suite of tools, including Wazuh, TheHive, Shuffle, and Sysmon, the system provides efficient threat detection, incident response, and investigation capabilities.

### Tools Used
* **[Wazuh](https://wazuh.com/):** An open-source security monitoring solution that provides real-time alerting, intrusion detection, and log analysis.
* **[DigitalOcean](https://www.digitalocean.com/):** A cloud computing platform used to host the Wazuh manager and TheHive.
* **[TheHive](https://strangebee.com/):** A security incident response platform that allows for efficient incident management, investigation, and reporting.
* **Shuffle:** A tool designed to enrich Indicators of Compromise (IOCs) using OSINT sources and trigger appropriate actions based on predefined rules.
* **Sysmon:** A system monitoring tool that provides detailed information about system processes, network connections, and file activity.




![Automation Workflow](https://github.com/xerone2/SOC-Automation/blob/main/Automation-Diagram.png)





### Workflow
  - **Event Collection:** The Wazuh agent on the Windows 10 client collects security-related events and forwards them to the Wazuh manager.
  -  **Alert Generation:** The Wazuh manager analyzes the incoming events and generates alerts based on predefined rules and signatures.
  -  **IOC Enrichment:** The Shuffle component enriches the IOCs associated with the alerts using OSINT sources like VirusTotal.
  -  **Alert Distribution:** The Shuffle sends the enriched alerts to TheHive for incident management.
  -  **Incident Investigation:** Security analysts in TheHive can investigate the incidents, gather additional evidence, and take appropriate response actions.
  -  **Notification:** The Shuffle can also send notifications to SOC analysts via email or other communication channels.

### Installation and Configuration
* [**Wazuh**](https://github.com/xerone2/SOC-Automation/blob/main/Wazuh-Installation.md)
* [**TheHive**](https://github.com/xerone2/SOC-Automation/blob/main/TheHive-Installation.md)
* [**Sysmon**](https://learn.microsoft.com/en-us/sysinternals/downloads/sysmon)
* [**Shuffle**](https://shuffler.io/)

### Additional Considerations
* **Rule Creation:** Develop and maintain effective Wazuh rules to detect a wide range of security threats.
* **Playbook Development:** Create playbooks in TheHive to automate incident response workflows and streamline investigations.
* **Integration with Other Tools:** Consider integrating the system with other security tools like SIEMs, EDR solutions, and SOAR platforms.
* **Continuous Monitoring and Improvement:** Regularly monitor the system's performance and make necessary adjustments to ensure optimal security posture.
