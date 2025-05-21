# 🛡️ Network Intrusion Detection System (NIDS) Development with Snort 3

[![Resultat](img/SNORT.jpg)](img/SNORT.jpg)

This project, successfully completed during my **#cadealpha** **#internship** in **#cybersecurity**, focused on designing, implementing, and testing a Network Intrusion Detection System (NIDS) using **Snort 3** for traffic monitoring and alert generation. I'm incredibly proud of the work accomplished and the valuable experience gained during this endeavor.

---

## 1. NIDS Tool Selection and Installation 🛠️

We leveraged **Snort 3** due to its robust capabilities, flexibility, and strong community backing. Our dedicated testing environment was set up on a **Kali Linux** virtual machine, or another compatible Linux distribution, for Snort 3's installation.

---

## 2. Snort 3 Configuration ⚙️

All Snort 3 dependencies, such as FlatBuffers, Boost, and DAQ, were meticulously installed and configured. In the `snort.lua` 📄 configuration file, we:

- Explicitly specified the network interface to be monitored (e.g., `eth0`, `wlan0`).
- Defined the `HOME_NET` and `EXTERNAL_NET` networks.
- Enabled essential inspection modules (e.g., `stream`, `HTTP`, `DNS`).
- Configured alert outputs, with logs directed to a file in formats like `fast`, `json`, or `unified2`.

---

## 3. Detection Rule Management 📝

We integrated existing Snort rule sets, including community rules or official ones if applicable. For **custom rule creation**, we:

- Identified straightforward yet relevant attack scenarios or suspicious activities, such as specific port scans, unauthorized service access attempts, or pattern detection in HTTP requests.
- Wrote tailored Snort 3 rules to detect these scenarios. Each custom rule was documented to explain its underlying logic and purpose.
- Managed the activation, deactivation, and prioritization of rules to refine the detection process.

---

## 4. Attack Simulation and Alert Analysis 🚨

Tools like **nmap**, **hping3**, **curl** (for simulating malicious web requests), and custom Python scripts were used to generate network traffic designed to deliberately trigger our configured rules.

- Snort 3 was run in monitoring mode to observe generated alerts in real-time or through log files.
- Each triggered alert underwent thorough analysis:
  - Which rule was triggered?
  - What was the root cause that led to the rule being triggered?
  - What crucial information did the alert contain (e.g., source/destination IP, ports, payload)?
  - We outlined potential response measures that would be implemented in a production environment for such alerts.

---

## Key Takeaways from the Project 💡

- **Incremental Approach:** We adopted an incremental approach, starting with a minimal setup and gradually introducing additional rules and features.
- **Rigorous Documentation:** Every installation step, configuration detail, and created rule was meticulously documented, proving invaluable for demonstrations and the final report.
- **Focus on Logic:** We prioritized understanding the "why" behind rules and alerts, rather than simply copying them.
- **Awareness of Limitations:** It's important to remember that Snort is a detection tool, not a complete prevention solution; it's part of a broader security strategy.

This comprehensive and ambitious project is now complete, providing valuable hands-on experience in the cybersecurity domain.
