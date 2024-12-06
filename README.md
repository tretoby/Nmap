# **NMAP**

## **Objective**

To use Nmap to scan a local network or a specific target to:  

- Discover active hosts and their open ports.  
- Identify the services running on these ports.  
- Perform a basic vulnerability analysis.  

---

## **Skills Learned**

- **Network Scanning**: Discovering active hosts, open ports, and services.  
- **Port and Service Identification**: Recognizing commonly used ports and services.  
- **Operating System Detection**: Identifying target operating systems from network responses.  
- **Vulnerability Analysis**: Detecting vulnerabilities using Nmap scripts (NSE).  
- **Command-Line Proficiency**: Executing Nmap commands efficiently.  
- **Data Interpretation**: Analyzing and understanding scan results.  
- **Reporting**: Summarizing findings into clear, actionable reports.  
- **Threat Identification**: Recognizing security risks and misconfigurations.  
- **Scripting Basics**: Automating scans and generating reports using scripts.  

---

## **Steps**

1. **Perform a Ping Scan**  
   Open the command line and perform a ping scan to discover active hosts on the network (`nmap -sn 192.168.1.0/24`).  
   - **Result**: 8 hosts were found.  
   ![Ping Scan Result](https://github.com/user-attachments/assets/f5ec890f-2f1d-4edc-97ac-81a19dabf991)

2. **Scan for Open Ports**  
   Scan for all open ports on a specific host. The command (`nmap -p 1-1000 192.168.1.10`) did not work, so I used (`nmap -Pn 192.168.0.10`).  
   - **Result**: 3 open ports were found: **53**, **80**, and **443**.  
   ![Open Ports](https://github.com/user-attachments/assets/21fd403d-87e2-484e-b85e-cc2009a0e7ac)

3. **Perform a Service Scan**  
   Conduct a service scan to identify what services are running on the open ports using (`sudo nmap -sS -A -Pn 1-1000 --reason 192.168.1.10`).  
   ![Service Scan Result](https://github.com/user-attachments/assets/e74e02db-14ce-4085-b0e1-833e7fab5113)

4. **Perform a Vulnerability Scan**  
   Perform a vulnerability scan on the target using (`nmap --script vuln -Pn 192.168.1.10`).  
   - **Result**: 1 vulnerability was found: **CVE-2011-1002**.  
   ![Vulnerability Found](https://github.com/user-attachments/assets/150fadfa-de86-4191-8923-40fdecba8341)  
   ![CVE Details](https://github.com/user-attachments/assets/9166ceea-0c1d-41df-b90f-213319a743f2)

---

## **Scan Report**

![Scan Report](https://github.com/user-attachments/assets/831679a0-c2b5-4f27-ad48-84441b7a0969)






