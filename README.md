# CyberSec_Task5_Wireshark_Analysis

## 🎯 Objective
To gain hands-on experience with a packet analyzer (Wireshark) by capturing live network traffic, applying filters, and identifying core network protocols.

## 🛠️ Tools Used
* **Operating System:** Windows 10/11
* **Tool:** Wireshark

## ⚙️ Steps Performed
1.  **Interface Selection:** Selected the active network interface (Wi-Fi/Ethernet) and started a live capture.
2.  **Traffic Generation:** Generated traffic by browsing the unencrypted website `http://example.com` and pinging `example.com`.
3.  **Capture and Save:** Stopped the capture and saved the data.
4.  **Protocol Filtering:** Applied various display filters to isolate and analyze specific traffic types.

## ✅ Summary of Findings (Protocols Identified)

The following three (or more) key protocols were successfully captured and identified in the traffic:

| Protocol | Filter Used | Key Detail Observed | Security Note |
| :--- | :--- | :--- | :--- |
| **DNS** | `dns` | Observed a standard **Query/Response** sequence used to translate the domain name into an IP address. | DNS is often unencrypted, making it vulnerable to monitoring. |
| **ICMP** | `icmp` | Observed **Echo Request** (ping) and **Echo Reply** packets, confirming network connectivity. | Often blocked by firewalls to prevent network mapping. |
| **HTTP** | `http` | Observed a **GET request** packet containing the full URL in **clear text**. | **CRITICAL:** Data (cookies, headers) is unencrypted and visible to anyone capturing traffic. |

## 💡 Deliverables and Learning Outcome

* **Packet Capture File:** The full capture file (`Network_Capture.pcap`) was saved but not uploaded due to its large size (100MB+).
* **Verification Screenshot:** Screenshot showing filtered HTTP traffic is attached.
* **Learning:** This task demonstrated the critical difference between **HTTP (unencrypted)** and **HTTPS (encrypted)** and reinforced the importance of packet analysis for network troubleshooting and security assessment.
