🕵️‍♂️ Splunk BOTSv1 Challenge: A Cybersecurity Investigation
Overview

This repository chronicles my journey through the Splunk Boss of the SOC v1 (BOTSv1) challenge—a Capture The Flag (CTF) style event designed to enhance threat hunting and incident response skills using Splunk. The challenge simulates real-world security incidents, providing a hands-on experience in analyzing and interpreting security data.
Table of Contents

    Challenge Summary

    Tools and Techniques

    Questions and Answers

    Key Learnings

    Conclusion

Challenge Summary

BOTSv1 presents a series of security incidents involving a fictitious hacktivist group, Po1s0n1vy, targeting Wayne Enterprises. The challenge is divided into multiple levels, each containing specific questions that require analyzing various data sources within Splunk to uncover the narrative of the attacks.
Tools and Techniques

    Splunk: Utilized for searching, monitoring, and analyzing machine-generated big data via a web-style interface.

    SPL (Search Processing Language): Employed to query and manipulate data within Splunk.

    Data Sources: Included HTTP logs, Sysmon logs, Suricata alerts, and firewall logs.

Questions and Answers
Level 1: Web Application Attacks

    What is the name of the company that makes the software that you are using for this competition?

        Answer: Splunk

        Insight: Familiarized with the Splunk interface and basic search functionalities.

    What is the likely IP address of someone from the Po1s0n1vy group scanning imreallynotbatman.com for web application vulnerabilities?

        Answer: 40.80.148.42

        Insight: Identified malicious scanning activity through analysis of HTTP logs and source IP addresses.

    What company created the web vulnerability scanner used by Po1s0n1vy?

        Answer: Acunetix

        Insight: Recognized scanner signatures within HTTP headers to determine the tool used.

    What content management system is imreallynotbatman.com likely using?

        Answer: Joomla

        Insight: Detected CMS-specific paths and files indicating the use of Joomla.

    What is the name of the file that defaced the imreallynotbatman.com website?

        Answer: poisonivy-is-coming-for-you-batman.jpeg

        Insight: Traced the defacement file through outbound HTTP requests from the web server.

    What fully qualified domain name (FQDN) is associated with this attack?

        Answer: prankglassinebracket.jumpingcrab.com

        Insight: Uncovered the attacker's staging server domain via analysis of firewall logs.

    What IPv4 address has Po1s0n1vy tied to domains that are pre-staged to attack Wayne Enterprises?

        Answer: 23.22.63.114

        Insight: Mapped multiple malicious domains to a single IP address, indicating a centralized attack infrastructure.

Level 2: Brute Force and Malware

    What IPv4 address is likely attempting a brute force password attack against imreallynotbatman.com?

        Answer: 23.22.63.114

        Insight: Detected brute force attempts by analyzing POST requests and form data patterns.

    What is the name of the executable uploaded by Po1s0n1vy?

        Answer: 3791.exe

        Insight: Identified the uploaded malware through process creation logs and command-line arguments.

    What is the MD5 hash of the executable uploaded?

        Answer: MIRANDA_PRI

        Insight: Retrieved the file's hash from Sysmon logs to assess its integrity and potential threats.

    What was the first brute force password used?

        Answer: superman

        Insight: Analyzed the sequence of login attempts to determine the initial password used in the attack.

    What was the correct password found in the brute force attack?

        Answer: batman

        Insight: Identified the successful login attempt by correlating login success events with form data.

    How many seconds elapsed between the time the brute force password scan identified the correct password and the compromised login?

        Answer: 0.73 seconds

        Insight: Calculated the rapid transition from password discovery to system compromise, highlighting the attacker's efficiency.

    How many unique passwords were attempted in the brute force attack?

        Answer: 5

        Insight: Counted distinct password attempts to understand the breadth of the brute force strategy.

Key Learnings

    SPL Proficiency: Enhanced ability to construct complex queries for data analysis.

    Threat Detection: Improved skills in identifying and interpreting indicators of compromise.

    Log Analysis: Gained experience in correlating events across multiple log sources to build a cohesive attack narrative.

    Incident Response: Developed a systematic approach to investigating and documenting security incidents.

Conclusion

Participating in the Splunk BOTSv1 challenge provided a practical and immersive experience in cybersecurity analysis. The exercise reinforced the importance of meticulous log examination and the application of analytical skills to uncover and understand sophisticated cyber threats.
