# 🎯 APT28 (Fancy Bear)  MITRE ATT&CK® TTPs Analysis

## 📌 Project Title

**APT28 (G0007) | MITRE ATT&CK® Technique Mapping & Analyst Walkthrough**

---

## 🧠 Summary / What It Does
This project breaks down how **APT28 (aka Fancy Bear)** operates using the **MITRE ATT&CK® Framework**. I mapped the group’s activity across tactics like **Reconnaissance, Resource Development, Initial Access, Execution, Persistence, Discovery, Lateral Movement, Exfiltration, and Defense Evasion** then analysed each phase through scenario-style questions.

The goal: to show that I can **interpret threat intelligence, map it to ATT&CK techniques, and identify what to hunt for (registry, PowerShell, proxies, remote services, etc.)** just like a SOC analyst or threat hunter would.

---

## ⚙️ Tools & Tech
- 🧩 **MITRE ATT&CK® Navigator v4.8.2**
- 💻 **Windows Event & Registry Analysis**
- 🧠 **Adversary Emulation & Threat Intel**
- 📊 **Layered ATT&CK mapping**
- 🗂️ **Markdown & GitHub Documentation**

---

## 🗂️ Features
- ✅ Visual mapping of **APT28’s TTPs** across multiple phases  
- ✅ Identified **execution, persistence, and exfiltration** behaviors  
- ✅ Recreated **analyst reasoning process** from SOC investigations  
- ✅ Highlighted **Windows and network-based detection points**  
- ✅ Demonstrates blue-team skills in **mapping, detection, and reporting**  

---
**🔍 Visual Walkthrough of ATT&CK Mapping**

### **1️⃣ – Initial Recon & Access**
 <img width="1809" height="169" alt="APT 28 MITRE ATT CK TTPS Question 1" src="https://github.com/user-attachments/assets/7c0b39d9-6806-4740-85d2-59f3f9ae42d8" />

<img width="1917" height="882" alt="APT 28 MITRE ATT CK TTPS Answer 1" src="https://github.com/user-attachments/assets/7914b509-041a-42ad-bfa7-13124e19b034" />


---

### **2️⃣ – Command & Scripting Interpreter Execution**
 <img width="1821" height="163" alt="APT 28 MITRE ATT CK TTPS Question 2" src="https://github.com/user-attachments/assets/3e6b5adb-2bc7-4ae8-9d8e-ece95feb0f8e" />

<img width="413" height="737" alt="APT 28 MITRE ATT CK TTPS Answer 2" src="https://github.com/user-attachments/assets/84f39987-b537-41d8-a299-bd2644b0f00a" />

🔍 APT28 often executes malicious payloads via these interpreters to run scripts and maintain stealth.

---

### **3️⃣ – User Execution Techniques**
 <img width="1805" height="180" alt="APT 28 MITRE ATT CK TTPS Question 3" src="https://github.com/user-attachments/assets/8e4f8cf3-c7e5-40e2-a96c-b27872bf51cf" />

<img width="441" height="133" alt="APT 28 MITRE ATT CK TTPS Answer 3" src="https://github.com/user-attachments/assets/33c5091f-778b-4199-aa95-60606b32325d" />

**Answer:** Malicious file and malicious link  
🎯 Classic phishing execution chain — the user triggers initial compromise.

---

### **4️⃣ – Resource Development / Infrastructure**
<img width="1812" height="140" alt="APT 28 MITRE ATT CK TTPS Question 4" src="https://github.com/user-attachments/assets/3feb81d9-9298-4118-8616-37f79ea064fb" />

<img width="441" height="245" alt="APT 28 MITRE ATT CK TTPS Answer 4" src="https://github.com/user-attachments/assets/57896ccd-3997-4f16-a529-374a98473e83" />

**Answer:** Domains, Web Services, and Email Accounts  
🧩 These resources help APT28 host payloads and deliver phishing campaigns.

---

### **5️⃣ – Persistence via Registry**
 <img width="1806" height="188" alt="APT 28 MITRE ATT CK TTPS Question 5" src="https://github.com/user-attachments/assets/03c55e9e-ea7d-40be-bb2e-48ba96b0245f" />

 <img width="701" height="134" alt="APT 28 MITRE ATT CK TTPS Answer 5" src="https://github.com/user-attachments/assets/0d5a6c84-df08-4442-a177-010922f23045" />

**Answer:** Registry Run Keys / Startup Folder  
⚙️ Used to maintain persistence by executing scripts on reboot.

---

### **6️⃣ – System Binary Proxy Execution**
<img width="1820" height="167" alt="APT 28 MITRE ATT CK TTPS Question 6" src="https://github.com/user-attachments/assets/02eef8ea-46dd-4821-87ea-2be96387b3fa" />

 <img width="705" height="306" alt="APT 28 MITRE ATT CK TTPS Answer 6" src="https://github.com/user-attachments/assets/9034b2a9-523c-4422-b456-89de153aef06" />

> **Answer:** Rundll32  
> 💡 APT28 executes malicious code through trusted Windows binaries to evade defenses.

---

### **7️⃣ – Discovery Techniques**
 <img width="1810" height="165" alt="APT 28 MITRE ATT CK TTPS Question 7" src="https://github.com/user-attachments/assets/9314410d-66bf-44cf-9e90-d502101e1c4b" />

<img width="255" height="108" alt="APT 28 MITRE ATT CK TTPS Answer 7" src="https://github.com/user-attachments/assets/a91138f4-389c-49ed-9563-fccc13706095" />

**Answer:** Network Sniffing  
🕵🏽‍♂️ Use of `tcpdump` and similar tools to capture credentials or internal network data.

---

### **8️⃣ – Lateral Movement**
<img width="1811" height="156" alt="APT 28 MITRE ATT CK TTPS Question 8" src="https://github.com/user-attachments/assets/af6fdf19-6d81-4d56-a7bf-705526afa95d" />

 <img width="495" height="184" alt="APT 28 MITRE ATT CK TTPS Answer 8" src="https://github.com/user-attachments/assets/26530b62-7486-428c-9ed8-d859ad60da16" />

**Answer:** SMB/Windows Admin Shares  
🔗 Used for lateral movement to spread within the network.

---

### **9️⃣ – Data Exfiltration Preparation**
<img width="1815" height="160" alt="APT 28 MITRE ATT CK TTPS Question 9" src="https://github.com/user-attachments/assets/f28d6221-64f6-4158-88e7-20d4d4d0b643" />

<img width="432" height="132" alt="APT 28 MITRE ATT CK TTPS Answer 9" src="https://github.com/user-attachments/assets/fc4584d0-429d-4660-8a59-56ae8a7f4f77" />

> **Answer:** SharePoint  
> 📂 The likely target for intellectual property theft or internal data exfiltration.

---

### **🔟 – Proxy & C2 Evasion**
 <img width="1815" height="214" alt="APT 28 MITRE ATT CK TTPS Question 10" src="https://github.com/user-attachments/assets/360f50e1-3583-44c2-8bda-2f8e49e6ef9a" />

 <img width="435" height="171" alt="APT 28 MITRE ATT CK TTPS Answer 10" src="https://github.com/user-attachments/assets/0a1095e7-ef1c-4ae4-bffc-2215bcb76bfb" />

**Answer:** External Proxy and Multi-hop Proxy  
🌍 Used to obscure C2 communications and bypass monitoring tools.

---

## 🚀 How to Recreate
1. Launch **MITRE ATT&CK® Navigator**.  
2. Open the **APT28 (G0007)** group layer.  
3. Map techniques across tactics like Execution, Persistence, and Discovery.  
4. Match findings with known Windows artifacts (registry keys, PowerShell logs, SMB shares, etc.).  
5. Capture screenshots and record reasoning like an analyst report.  

---

## ✅ What I Learned
- How to **analyze APT behaviors** using ATT&CK mappings  
- How different phases connect: *Recon → Execution → Persistence → Exfiltration*  
- How **APT28 uses Windows binaries** (e.g., `rundll32`) for stealth  
- The value of **network monitoring and proxy analysis** for C2 detection  
- How to **document adversary activity visually and clearly**  

---

## 📚 Resources
- [MITRE ATT&CK® Framework](https://attack.mitre.org/)  
- [APT28 Threat Group | G0007](https://attack.mitre.org/groups/G0007/)  
- [CISA Reports on APT28](https://www.cisa.gov/)  
- [Microsoft Threat Intelligence Blog | APT28 Overview](https://www.microsoft.com/security/blog/)  
- [TryHackMe: MITRE ATT&CK Labs](https://tryhackme.com/)  

---

## 🙌 Credits / Acknowledgements
- **MITRE ATT&CK®** for the framework  
- **Threat Intel & CTI community** for ongoing research  
- **TryHackMe / Blue Team Labs** for structured TTP-based labs  
- **All screenshots and analysis**: created and documented by me  

---

## 💡 Why This Project Matters
This project demonstrates my ability to:
- 🧠 Think like an **analyst** and connect the dots between threat behavior and system artifacts  
- 🎯 Understand **APT methodology** and **defensive detection strategies**  
- 🔍 Use **MITRE ATT&CK** not just as a framework, but as a hands-on investigation tool  
- 📑 Communicate findings in a **clear, visual, and technical** way suitable for SOC environments  

It’s the perfect showcase of **blue-team mindset + analytical clarity**. 💪🏽
