## Penetration Testing Lab with Kali Linux

The goal of this project was to perform a penetration test on the OWASP Juice Shop, a vulnerable web application, to identify potential vulnerabilities, analyze the system, and extract sensitive data. This project demonstrates key penetration testing skills, including reconnaissance, vulnerability scanning, exploitation, and documentation.

---

### **Table of Contents**
1. [Overview](#overview)
2. [Tools Used](#tools-used)
3. [Methodology](#methodology)
    - [Reconnaissance](#1-reconnaissance)
    - [Vulnerability Scanning](#2-vulnerability-scanning)
    - [Exploitation](#3-exploitation)
4. [Findings](#findings)
5. [Screenshots](#screenshots)
6. [Conclusion](#conclusion)

---

### **Overview**
OWASP Juice Shop is a deliberately insecure web application used for security training. This project focuses on identifying misconfigurations, exploiting vulnerabilities, and documenting the penetration testing process. Key tasks included:
- Discovering open ports and services.
- Identifying potential vulnerabilities using automated scanners.
- Extracting sensitive data using exploitation techniques.

---

### **Tools Used**
- **Kali Linux**: Primary platform for penetration testing.
- **Nmap**: Network mapping and service enumeration.
- **Nikto**: Web server vulnerability scanner.
- **wget** and **curl**: File retrieval and analysis.
- **OWASP Juice Shop**: Vulnerable target application.

---

### **Methodology**

#### **1. Reconnaissance**
- Performed a network scan using `nmap` to identify open ports and services.
- Found the HTTP service running on port 3000, hosting the OWASP Juice Shop application.
  
#### **2. Vulnerability Scanning**
- Used `Nikto` to scan for vulnerabilities on the HTTP service.
- Discovered:
  - Misconfigured headers.
  - Potentially interesting files (e.g., `.pem`, `.tar.gz`, `.bak`).
  - Directory listings that exposed sensitive files.

#### **3. Exploitation**
- Explored files using tools like `wget` and `curl` to retrieve and analyze the contents.
- Found:
  - `acquisitions.md` containing confidential mock data.
  - `encrypt.pyc`, which hinted at encrypted content requiring decompilation.


---

### **Findings**
1. **Vulnerabilities Identified**:
   - Misconfigured headers, exposing sensitive information.
   - Directory listing enabled, leading to accessible sensitive files.
2. **Exploitation Results**:
   - Extracted mock confidential data from `acquisitions.md`.
   - Decrypted potential files for further analysis.

---

### **Screenshots**
- **Nmap Scan**: Showing open ports and services.
- **Nikto Scan**: Displaying vulnerabilities and interesting files.
- **Exploration**: Screenshots of retrieved files and their analysis.

---

### **Conclusion**
This project demonstrates the ability to:
- Use penetration testing tools effectively to identify and exploit vulnerabilities.
- Document findings in a structured and professional manner.
- Highlight the importance of securing web applications against common misconfigurations and exploits.

