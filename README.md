# SOC Analyst Homelab — Wazuh SIEM with Windows Agent

![Lab Architecture](images/architecture-diagram.png)

A fully functional mini Security Operations Center (SOC) built from scratch using **free and open-source tools** to practice real-world endpoint monitoring, log collection, and threat detection.

### Project Goal
Monitor a Windows 11 endpoint, collect logs in real time, and detect suspicious activity using **Wazuh** — one of the most popular open-source SIEM + XDR platforms.

### Lab Architecture
![Architecture Overview](images/soc-homelab-diagram.png)

| Machine          | Role                              | OS            |
|------------------|-----------------------------------|---------------|
| Ubuntu Server    | Wazuh Manager + Dashboard        | Ubuntu 22.04  |
| Windows 11       | Victim / Monitored Endpoint       | Windows 11    |
| Kali Linux       | Attack simulation & testing       | Kali Linux    |

### VirtualBox Overview
![VirtualBox VMs](images/virtualbox-vms.png)

## Steps Implemented

### 1. Installed Wazuh on Ubuntu Server (All-in-One Deployment)
![Wazuh Services Starting](images/wazuh-services-starting.png)
- Deployed Wazuh Manager, Filebeat, and Dashboard  
- Verified all services active and dashboard accessible at `https://<server-ip>`

### 2. Configured Windows 11 as Monitored Endpoint
![Wazuh Windows Agent Installation](images/windows-agent-install-1.png)
![Agent Enrollment & Service Start](images/windows-agent-install-2.png)
- Downloaded and installed the official Wazuh Windows agent  
- Enrolled agent using manager IP and enrollment key  
- Confirmed `wazuh-agent` service running

### 3. Validated Agent Connectivity in Wazuh Dashboard
![Agent Appears as Active](images/agent-active-dashboard.png)
- Agent successfully registered and showed as **Active**  
- Real-time logs flowing from Windows 11 → Wazuh server  
- Tested basic event generation and confirmed visibility

### Results
- Wazuh successfully detected activities on the Windows endpoint  
- Windows agent stayed connected and continuously forwarded logs  
- Demonstrated the full SOC workflow: **Attack → Logging → Detection → Monitoring**

### Skills & Knowledge Gained
By completing this homelab I strengthened the following skills (directly applicable to SOC Analyst roles):

- Hands-on experience with SIEM (Wazuh)  
- Deploying and managing endpoint agents (Windows)  
- Log collection, parsing, and real-time monitoring  
- Understanding attack → detect → respond workflow  
- Building a realistic SOC environment from scratch using free tools

### Tools Used
- Wazuh (open-source SIEM/XDR)  
- VirtualBox  
- Ubuntu Server 22.04  
- Windows 11  
- Kali Linux

### Next Steps (Planned Expansions)
- Add Linux endpoint agents  
- Integrate Sysmon + custom Wazuh rules  
- Add TheHive/Shuffle for incident response (SOAR)  
- Active Directory + Group Policy integration  
- Custom decoders and alerts

---
**Perfect portfolio project for Junior SOC Analyst, Blue Team, or Cybersecurity Analyst roles**

### Repository Contents
- `home lab setup.pdf` – Original project documentation  
- `/images/` – All screenshots and diagrams  
- `README.md` – This file

### Connect with Me
🔗 Add this project to your resume and LinkedIn — recruiters love real hands-on homelabs!

---
**Topics (add these in GitHub):**  
`wazuh` `siem` `soc-analyst` `homelab` `cybersecurity` `blue-team` `endpoint-security` `threat-detection` `windows-agent` `open-source`

---
**Built with free tools • 100% reproducible • Great for learning and interviews**
