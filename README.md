# 📄 Understanding the Discrepancy in Login Count Tracking for Microsoft Accounts in Windows Systems  

## 📌 Overview  

This document investigates an observed discrepancy in **Windows login count tracking** for **Microsoft cloud accounts**. While local user accounts have their login counts accurately recorded in the **Security Accounts Manager (SAM) file**, Microsoft cloud accounts **do not store login counts in the same manner** within the registry.  

This analysis explores the **root cause** of this issue, the **mechanisms behind Windows authentication**, and **forensic techniques** for tracking Microsoft account logins when the registry lacks sufficient data.  

---

## 🔍 Key Findings  

### ❌ Missing Login Counts for Microsoft Accounts  
- **Local accounts** store login counts in the **SAM database** (`C:\Windows\System32\config\SAM`).  
- **Microsoft cloud accounts** **do not** record login counts in the SAM database.  
- **Cloud authentication** methods affect how Windows logs Microsoft account login activity.  

### 🛠️ Alternative Methods for Tracking Microsoft Account Logins  

1️⃣ **Windows Event Logs**  
   - **Event ID 4624** (Windows Event Viewer) logs successful logins for both local and cloud-based Microsoft accounts.  

2️⃣ **Microsoft Account Activity Page**  
   - Available at **[account.microsoft.com/security](https://account.microsoft.com/security)**, displaying the **full login history** for Microsoft accounts.  

3️⃣ **Registry Keys**  
   - **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Authentication\LogonUI**  
   - Contains some **authentication-related** data but does not store login counts.  

---

## 🏁 Conclusion  

The **absence of login count data for Microsoft accounts** in the Windows registry is due to **cloud-based authentication mechanisms**. Forensic investigators must **rely on alternative sources** such as **Event Logs** and the **Microsoft Account Activity Page** to track login activities effectively.  

Understanding these **discrepancies** is critical for **Windows forensic investigations**, ensuring accurate tracking of **authentication events** in forensic cases.  

📌 **For more details, refer to the full report attached.**  

---

## 🖋️ Author  

**🔹 Name:** Hun13r  
**🔹 Company:** Greaton Forensics  
**🔹 Email:** [admin@greaton.co.uk](mailto:admin@greaton.co.uk)  
