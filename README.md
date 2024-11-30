**NMAP**

**Objective**

To use Nmap to scan a local network or a specific target to:

Discover active hosts and their open ports.
Identify the services running on these ports.
Perform a basic vulnerability analysis.

**Skills Learned**

Network Scanning: Discovering active hosts, open ports, and services.

Port and Service Identification: Recognizing commonly used ports and services.

Operating System Detection: Identifying target operating systems from network responses.

Vulnerability Analysis: Detecting vulnerabilities using Nmap scripts (NSE).

Command-Line Proficiency: Executing Nmap commands efficiently.

Data Interpretation: Analyzing and understanding scan results.

Reporting: Summarizing findings into clear, actionable reports.

Threat Identification: Recognizing security risks and misconfigurations.

Scripting Basics: Automating scans and generating reports using scripts.

**Steps**:
open command line and perform a ping scan to discover active host on the network ( nmap -sn 192.168.1.0/24)
8host were found

![image](https://github.com/user-attachments/assets/f5ec890f-2f1d-4edc-97ac-81a19dabf991)

now I will scan all open ports on my local network (nmap -p 1-1000 192.168.1.10) did not work so I used (nmap -Pn 192.168.0.10)
3 open ports were found 53, 80, 443

![image](https://github.com/user-attachments/assets/21fd403d-87e2-484e-b85e-cc2009a0e7ac)

perform a service scan using ( sudo nmap -sS -A -Pn 1-1000 --reason 192.168.1.10)

![image](https://github.com/user-attachments/assets/e74e02db-14ce-4085-b0e1-833e7fab5113)

perform a vulnerability scan  using (nmap --script vuln -Pn 192.168.1.10)
not showing any vulnerabilities 

![image](https://github.com/user-attachments/assets/5b35d5e8-cc9d-490c-b51a-e2252a522a5c)

**Scan Report**
![image](https://github.com/user-attachments/assets/6c437211-650a-474e-af5c-70059462bdd7)


