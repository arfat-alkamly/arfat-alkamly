# 🧪 Cybersecurity Labs

> **توثيق المختبرات الافتراضية وتجارب التدريب العملي**

---

## 🏗️ Lab Infrastructure Overview

### البنية التحتية للمختبرات

| المكون | التفاصيل |
|:---|:---|
| **منصة المحاكاة** | VMware Workstation / VMware ESXi |
| **شبكة العزل** | VLANs معزولة — لا اتصال بالشبكة الخارجية |
| **أنظمة الهجوم** | Kali Linux (آخر إصدار) |
| **أنظمة الهدف** | Windows Server, Windows 10, Ubuntu Server, Metasploitable |
| **أدوات المراقبة** | Wireshark, Snort, Zeek, Splunk (trial) |

---

## 🎯 Active Labs

### Lab 1: Web Application Penetration Testing

**المنصة:** DVWA, WebGoat, Juice Shop  
**الأدوات:** Burp Suite, OWASP ZAP, SQLMap, Nikto  
**الحالة:** 🟡 قيد التقدم

#### السيناريو
اختبار تطبيقات ويب متعمدة الضعف لفهم واستغلال ثغرات OWASP Top 10.

#### المهارات المكتسبة
- **Injection Attacks** — SQL Injection, Command Injection, LDAP Injection
- **Broken Authentication** — Bypass login, Session hijacking
- **Sensitive Data Exposure** — Information disclosure, Insecure direct object references
- **Security Misconfiguration** — Default credentials, Directory listing
- **XSS (Cross-Site Scripting)** — Stored, Reflected, DOM-based
- **CSRF (Cross-Site Request Forgery)** — Token bypass, State-changing attacks

#### التوثيق
- [ ] كتابة تقرير مفصل لكل ثغرة
- [ ] توثيق خطوات الاستغلال والحلول
- [ ] إنشاء checklist للاختبار

---

### Lab 2: Active Directory Attack & Defense

**المنصة:** Windows Server 2019 (DC), Windows 10 (Workstation)  
**الأدوات:** BloodHound, Mimikatz, CrackMapExec, Impacket, Responder  
**الحالة:** 🟡 قيد التقدم

#### السيناريو
محاكاة بيئة Active Directory حقيقية وتنفيذ هجمات متقدمة مع فهم آليات الدفاع.

#### المهارات المكتسبة
- **Reconnaissance** — LDAP enumeration, SMB enumeration, DNS enumeration
- **Credential Access** — Kerberoasting, AS-REP Roasting, DCSync
- **Lateral Movement** — Pass-the-Hash, Pass-the-Ticket, WMI/PSExec
- **Privilege Escalation** — Token impersonation, Unquoted service paths
- **Persistence** — Golden Ticket, Silver Ticket, ACL abuse
- **Defense** — Event log analysis, SIEM rule creation

#### التوثيق
- [ ] رسم خريطة Attack Path باستخدام BloodHound
- [ ] توثيق كل تقنية مع الـ MITRE ATT&CK ID
- [ ] كتابة دليل دفاعي مقابل

---

### Lab 3: Network Traffic Analysis

**المنصة:** Custom network with multiple VMs  
**الأدوات:** Wireshark, Zeek, Snort, NetworkMiner  
**الحالة:** 🟢 نشط

#### السيناريو
التقاط وتحليل حركة مرور الشبكة لتحديد الأنماط المشبوهة والهجمات.

#### المهارات المكتسبة
- **Protocol Analysis** — TCP/IP, HTTP/HTTPS, DNS, DHCP deep dive
- **Malware Traffic** — Identifying C2 communications, beaconing
- **Attack Detection** — Port scanning, brute force, data exfiltration
- **Forensic Analysis** — PCAP analysis for incident response

#### التحديات المنجزة
- [x] تحليل هجوم Nmap scan
- [x] كشف محاولة brute force على SSH
- [x] تحديد اتصال C2 مشبوه
- [ ] تحليل هجوم Man-in-the-Middle

---

### Lab 4: Wireless Security Assessment

**المنصة:** Kali Linux + Wireless Adapter (Monitor Mode)  
**الأدوات:** Aircrack-ng suite, Wireshark, Reaver, Wifite  
**الحالة:** 🟡 قيد التقدم

#### السيناريو
اختبار أمن الشبكات اللاسلكية وفهم نقاط الضعف في بروتوكولات التشفير.

#### المهارات المكتسبة
- **WEP Cracking** — Statistical attacks, Fragmentation
- **WPA/WPA2 Cracking** — Dictionary attacks, Handshake capture
- **WPA3 Analysis** — SAE handshake, Dragonblood vulnerabilities
- **Rogue Access Points** — Evil twin, Karma attacks
- **Wireless Reconnaissance** — SSID discovery, Client enumeration

---

### Lab 5: Malware Analysis Sandbox

**المنصة:** Cuckoo Sandbox, REMnux, FlareVM  
**الأدوات:** Ghidra, IDA Free, x64dbg, YARA, PEStudio  
**الحالة:** ⚪ مخطط

#### السيناريو
تحليل البرمجيات الخبيثة في بيئة معزولة لفهم سلوكها وآليات عملها.

#### المهارات المخططة
- **Static Analysis** — PE structure, Imports/Exports, Strings analysis
- **Dynamic Analysis** — Behavior monitoring, API hooking
- **Memory Forensics** — Volatility, Rekall for memory dumps
- **Reverse Engineering** — Assembly analysis, Decompilation
- **YARA Rules** — Creating detection signatures

---

## 📊 Lab Progress Tracker

| المختبر | الهجوم | الدفاع | التوثيق | المستوى |
|:---|:---:|:---:|:---:|:---:|
| Web App Pentesting | 🟡 60% | ⚪ 0% | 🟡 30% | متوسط |
| Active Directory | 🟡 40% | ⚪ 0% | 🟡 20% | متقدم |
| Network Analysis | 🟢 75% | 🟡 50% | 🟡 40% | متوسط |
| Wireless Security | 🟡 30% | ⚪ 0% | ⚪ 0% | مبتدئ |
| Malware Analysis | ⚪ 0% | ⚪ 0% | ⚪ 0% | مخطط |

---

## 📝 Lab Write-ups Policy

> **مبدئي في التوثيق:** كل تجربة في المختبر يجب أن تُوثق بالتفصيل. التوثيق ليس مجرد سجل، بل هو:
> - **مرجع للرجوع** عند مواجهة سيناريو مشابه
> - **محتوى تعليمي** يمكن مشاركته مع المجتمع
> - **دليل دفاعي** لفهم كيفية الحماية من كل هجوم

### صيغة التوثيق القياسية
1. **العنوان والوصف** — ما هو السيناريو؟
2. **البيئة** — ما الأدوات والأنظمة المستخدمة؟
3. **خطوات التنفيذ** — بالتفصيل مع الأوامر
4. **النتائج** — ما الذي تم إنجازه؟
5. **الدروس المستفادة** — ما الجديد الذي تعلمته؟
6. **الحماية** — كيف يمكن الدفاع ضد هذا الهجوم؟

---

## 🎯 Future Lab Plans

### Cloud Security Lab
- AWS/Azure free tier environment
- IAM misconfiguration exploitation
- S3 bucket enumeration and exploitation
- Container escape scenarios

### IoT Security Lab
- Raspberry Pi as IoT device
- Firmware analysis and extraction
- UART/JTAG debugging
- MQTT and CoAP protocol analysis

### SCADA/OT Security Lab
- Modbus protocol simulation
- DNP3 traffic analysis
- Industrial control system vulnerabilities
- Network segmentation for OT environments
