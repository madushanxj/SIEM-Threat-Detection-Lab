# SIEM-Threat-Detection-Lab: Splunk & Atomic Red Team

This project emulates a mini Security Operations Center (SOC) environment to showcase real-world threat detection using Splunk Enterprise, Sysmon, Splunk Universal Forwarder, and Atomic Red Team. It highlights end-to-end attacker simulation and detection mapped to the MITRE ATT&CK framework, including alerting, reporting, and correlation logic.

## Project Overview
A Windows 10 virtual machine was configured as the target endpoint (victim), while an Ubuntu Server VM hosted Splunk Enterprise for log ingestion and analysis. Splunk Universal Forwarder and Sysmon (with SwiftOnSecurity configuration) were used for comprehensive telemetry. Atomic Red Team was employed to safely simulate adversarial behaviors such as:

-Brute-force login attempts.

-Malicious PowerShell execution.

-Registry-based persistence techniques.

Splunk dashboards, alerts, and correlation searches were created to detect and respond to these simulated threats in real time.

##Tools & Technologies

-Splunk Enterprise (SIEM Platform)

-Splunk Universal Forwarder

-Sysmon (with SwiftOnSecurity config)

-Atomic Red Team (Invoke-AtomicRedTeam)

-VirtualBox

-Windows 10 VM (Victim)

-Ubuntu Server 22.04 VM (SIEM Server)

## Key MITRE ATT&CK Techniques Detected

| Use Case                                     | Technique ID          | Technique Name                                      |
|----------------------------------------------|-----------------------|-----------------------------------------------------|
| Suspicious PowerShell Execution              | T1059.001             | Command & Scripting Interpreter: PowerShell         |
| Brute Force Login Attempts                   | T1110.001             | Brute Force: Password Guessing                      |
| Registry Key Persistence                     | T1547.001    	       | Boot/Logon Autostart Execution: Registry Keys       |
| Brute Force Followed by Successful Login     | T1110 + T1078	       | Valid Accounts Used After Brute Force               |
| PowerShell Followed by Registry Persistence  | T1059.001 + T1547.001 | Multi-Stage Persistence with Scripting              |

## Splunk Features Implemented

1. **Set up VMs** with VirtualBox: Windows 10 (Victim machine) and Ubuntu Server (Splunk)
2. **Install Splunk Enterprise** on Ubuntu Server
3. **Install Splunk Universal Forwarder + Sysmon** on Windows 10 VM
4. **Ingest logs into Splunk**, verify via search
5. **Simulate attacks** using Atomic Red Team on Windows
6. **Visualize detections** in dashboards
7. **Set alerts** for real-time detection
8. **Run correlation SPL queries** and save as reports

## Key Outcomes
- Enabled centralized log collection and endpoint visibility

- Simulated real-world attacks aligned with MITRE ATT&CK

- Developed detection content: dashboards, alerts, and SPL rules

- Gained hands-on experience in SIEM deployment and detection engineering

## Visual Evidence

![Triggered_Alerts_List](https://github.com/user-attachments/assets/760b49ea-2fab-4569-938e-25d810956692)
![Sysmon_Event_Logs_In_Splunk](https://github.com/user-attachments/assets/b3e7e62b-43ad-4676-8b6b-4fc8c914ef89)
![Splunk_Reports_List_View](https://github.com/user-attachments/assets/793094fa-d04b-44c9-b329-9734c291f4cc)
![Splunk_Forwarder_inputs_conf](https://github.com/user-attachments/assets/7162dca9-8f3e-419c-94a0-273d75a1b78f)
![Report2_PowerShell_Registry_Persistence](https://github.com/user-attachments/assets/3bf6a42a-b0d3-449c-9620-ccbe63f797cd)
![Report1_Brute_Force_Attack](https://github.com/user-attachments/assets/7c129794-e418-4fc2-8068-b56cf1a75dda)
![Panel3_PowerShell_Suspicion_Score_Before](https://github.com/user-attachments/assets/67e9c233-c59e-4ddc-a7d6-5a49b1a8c90a)
![Panel3_PowerShell_Suspicion_Score_After](https://github.com/user-attachments/assets/093d53b1-0184-4e3f-a5ee-43b92f232bc6)
![Dashboard_Initial_State](https://github.com/user-attachments/assets/92c22249-6901-43da-af6f-02cbd923bbf4)
![Dashboard_After_Test3](https://github.com/user-attachments/assets/78414001-8e69-4f5d-8ae8-2ca877ca9bb8)
![Creating_Dashboard](https://github.com/user-attachments/assets/0dd3002f-07b9-4e30-af3b-576591e61bf9)
![AtomicRedTeam_Running_Tests](https://github.com/user-attachments/assets/c53374af-eb6c-4d49-a05d-26f5c6520d00)
![Adding_Panel_To_Dashboard](https://github.com/user-attachments/assets/a641d898-e6e1-4445-9131-c845878b1cc7)

## Resources

- [Atomic Red Team](https://github.com/redcanaryco/atomic-red-team)
- [SwiftOnSecurity Sysmon Config](https://github.com/SwiftOnSecurity/sysmon-config)
- [MITRE ATT&CK Framework](https://attack.mitre.org/)
- [Splunk Enterprise](https://www.splunk.com/)
- [Splunk Universal Forwarder](https://www.splunk.com/en_us/download/universal-forwarder.html)

