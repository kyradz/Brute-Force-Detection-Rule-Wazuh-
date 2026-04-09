# Brute Force Detection Rule (Wazuh)<br>
This project focuses on detecting brute force attacks using Wazuh by creating a custom detection rule based on log analysis.<br>
<br>
<br>
# Objective<br>
The goal of this project is to simulate and detect brute force attempts by analyzing authentication logs and triggering alerts a custom Wazuh rule<br>
<br>
# What I Learned<br>
-How to analyze authentication logs<br>
-How to identify brute force patterns<br>
-How to create custom Wazuh rules<br>
<br>
<br>
# Concept<br>
Brute force attacks consist of multiple failed login attempts targeting a system.<br>
This project detects such behavior by monitoring repeated failed authentication attempts within a short time frame.<br>
<br>
<br>
# Technologies<br>
-Wazuh (SIEM & log analysis)<br>
-Kali Linux (attack simulation)<br>
-Linux (log source & environment)<br>
-Windows (target system)<br>
-Hydra (brute force attack simulation)<br>
<br>
<br>
# How it Works<br>
1.Monitors authentication logs<br>
2.Detects repeated failed login attempts<br>
3.Triggers a custom alert level 13 when 3 failed logins within a minute are detected<br>
<br>
<br>
# Detailed Explanation<br>
1.Controlled brute force simulation<br>
A controlled brute force attack was performed to identify the relevant SID associated with failed login attempts on the target system.<br>
<br>
![image alt](https://github.com/kyradz/Brute-Force-Detection-Rule-Wazuh-/blob/ca0a0d40fc8d69487ef638d11abd3ca715da02be/SID%20Windows%20Machine.png) <br>
<br>
2.Custom rule creation<br>
A custom Wazuh rule was created using the identified SID to detect repeated failed authentication attempts.<br>
<br>
![image alt](https://github.com/kyradz/Brute-Force-Detection-Rule-Wazuh-/blob/ca0a0d40fc8d69487ef638d11abd3ca715da02be/custom%20rule.png)<br>
<br>
3.Detection and alert generation<br>
After re-running the attack, the system successfully triggered an alert when 3 failed login attempts were detected within 1 minute.<br>
<br>
![image alt](https://github.com/kyradz/Brute-Force-Detection-Rule-Wazuh-/blob/ca0a0d40fc8d69487ef638d11abd3ca715da02be/Windows%20auth%20brute%20force%20attack.png)
![image alt](https://github.com/kyradz/Brute-Force-Detection-Rule-Wazuh-/blob/ca0a0d40fc8d69487ef638d11abd3ca715da02be/Threat%20Hunting%20Event.png)
