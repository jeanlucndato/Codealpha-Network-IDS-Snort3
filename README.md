# 🛡️ Network Intrusion Detection System (NIDS) Development with Snort 3

[![Resultat](img/SNORT.jpg)](img/SNORT.jpg)

This project, successfully completed during my **CodeAlpha internship** in **cybersecurity**, focused on designing, implementing, and testing a Network Intrusion Detection System (NIDS) using **Snort 3** for traffic monitoring and alert generation. I'm incredibly proud of the work accomplished and the valuable hands-on experience gained during this endeavor.

---

## 1. NIDS Tool Selection and Environment Setup 🛠️

We opted for **Snort 3** due to its powerful capabilities, flexibility, and strong community support. My dedicated testing environment was set up using **two virtual machines**:

- A **Kali Linux VM** served as the attacker machine, used for simulating various network attacks.
- An **Ubuntu VM** was configured as the target machine, where Snort 3 was installed and actively monitored network traffic.

---

## 2. Snort 3 Configuration ⚙️

All Snort 3 dependencies, such as FlatBuffers, Boost, and DAQ, were meticulously installed and configured. In the `snort.lua` configuration file, we:

- Explicitly specified the **network interface** to be monitored (e.g., `eth0`).
- Defined the **`HOME_NET`** and **`EXTERNAL_NET`** networks to properly delineate internal and external traffic.
- Enabled essential **inspection modules** (e.g., `stream`, `HTTP`, `DNS`) for deep packet inspection.
- Configured **alert outputs**, with logs directed to a file in formats like `fast`, `json`, or `unified2`.

---

## 3. Detection Rule Management 📝

We integrated existing Snort rule sets and also developed custom rules. To keep our rule sets updated and efficient, we leveraged **PulledPork 3** to automatically download, manage, and optimize Snort rules. For **custom rule creation**, we:

- Identified straightforward yet relevant attack scenarios or suspicious activities, such as specific port scans, unauthorized service access attempts, or pattern detection in HTTP requests.
- Wrote tailored **Snort 3 rules** to detect these scenarios, ensuring proper syntax and functionality.
- Each custom rule was documented to explain its underlying logic and purpose, aiding in future analysis and refinement.
- Managed the activation, deactivation, and prioritization of rules to refine the detection process, minimizing false positives and enhancing accuracy.

---

## 4. Attack Simulation and Alert Analysis 🚨

Tools like **nmap**, **hping3**, **curl** (for simulating malicious web requests), and custom Python scripts were used from the Kali Linux VM to generate network traffic designed to deliberately trigger our configured rules on the Ubuntu target.

- Snort 3 was run in monitoring mode to observe generated alerts in real-time or through log files.
- Each triggered alert underwent thorough analysis:
  - Which rule was triggered?
  - What was the root cause that led to the rule being triggered?
  - What crucial information did the alert contain (e.g., source/destination IP, ports, payload)?
  - We outlined potential response measures that would be implemented in a production environment for such alerts.

---

[![the result](img/image.gif)](img/image.gif)

## Key Takeaways and Project Success 💡

This comprehensive and ambitious project was a great success. All the configurations, rules, and simulations worked as expected, demonstrating a strong grasp of NIDS principles and Snort 3 implementation. This project provided invaluable **hands-on experience** in the cybersecurity domain, successfully demonstrating the capabilities of Snort 3 as a NIDS.

- **Incremental Approach:** We adopted an incremental approach, starting with a minimal setup and gradually introducing additional rules and features. This allowed for systematic troubleshooting and verification.
- **Rigorous Documentation:** Every installation step, configuration detail, and created rule was meticulously documented, proving invaluable for demonstrations and the final report.
- **Focus on Logic:** We prioritized understanding the "why" behind rules and alerts, rather than simply copying them, which deepened our comprehension of attack vectors and detection strategies.
- **Awareness of Limitations:** It's important to remember that Snort is a detection tool, not a complete prevention solution; it's part of a broader security strategy.
