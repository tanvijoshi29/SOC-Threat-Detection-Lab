# SOC Threat Detection & Security Monitoring Lab

## Overview

Designed and implemented a virtualized Security Operations Center (SOC) lab for centralized log analysis, endpoint telemetry monitoring, and threat detection using Splunk Enterprise, Wazuh, and Sysmon.

The environment simulates real-world SOC workflows including authentication monitoring, suspicious PowerShell detection, process monitoring, and live security event correlation across Windows and Linux systems.

---

# Key Features

- Centralized SIEM-based log collection
- Real-time security monitoring
- Windows endpoint telemetry analysis
- Suspicious PowerShell detection
- Failed authentication monitoring
- Sysmon process creation logging
- Threat hunting using Splunk SPL queries
- Wazuh-based alert monitoring
- Virtualized SOC infrastructure deployment

---

# Tech Stack

| Category | Technologies |
|---|---|
| SIEM | Splunk Enterprise |
| Threat Monitoring | Wazuh |
| Endpoint Telemetry | Sysmon |
| Operating Systems | Windows 11, Ubuntu Server |
| Virtualization | Oracle VirtualBox |
| Log Sources | Windows Security Logs, Sysmon Operational Logs |

---

# Architecture

+----------------------+
|  Windows Endpoint    |
|----------------------|
| Sysmon               |
| Windows Event Logs   |
+----------+-----------+
           |
           v
+----------------------+
|     Wazuh Agent      |
+----------+-----------+
           |
           v
+----------------------+
|   Ubuntu Wazuh SOC   |
|----------------------|
| Wazuh Manager        |
| Alert Processing     |
+----------+-----------+
           |
           v
+----------------------+
|  Splunk Enterprise   |
|----------------------|
| Threat Hunting       |
| Log Analysis         |
| Event Correlation    |
+----------------------+
