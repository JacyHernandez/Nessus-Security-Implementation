# Nessus Essentials Installation and SMB Configuration Guide

This guide provides step-by-step🚶🏽‍♂️‍➡️instructions to install **Nessus Essentials**, perform a Host Discovery Scan, and configure SMB settings using the Group Policy Editor.

# What is Nessus Tenable Essentials?

Nessus Tenable Essentials is a free vulnerability scanning tool 🔍 designed to help individuals and organizations identify weaknesses in their systems. It allows you to assess devices on your network for security risks, giving you actionable insights to protect against potential threats.

Think of it as a security guard for your digital space always on the lookout for vulnerabilities and ready to provide solutions to keep your systems safe 🔐.

## What Does Nessus Tenable Essentials Do?

### Detect Vulnerabilities:
- Identifies weaknesses in software, misconfigurations, and outdated systems.

### Prioritize Risks:
- Uses the Common Vulnerability Scoring System (CVSS) to categorize vulnerabilities by severity, helping you focus on the most critical issues.

### Provide Remediation Steps:
- Offers clear descriptions of vulnerabilities and actionable solutions to fix them.

### Enhance Security Posture:
- Regular scans ensure your systems remain protected against emerging threats.

## Why is Nessus Tenable Essentials Important?

Cyber threats are constantly changing. Tools like Nessus Essentials are crucial for:

- **Early Threat Detection**: Identifying vulnerabilities before attackers can exploit them.
- **Informed Decision-Making**: Providing detailed reports that guide effective security measures.
- **Skill Building**: A hands-on way to learn about cybersecurity and vulnerability management.
- **Network Health**: Maintaining a secure and stable environment by fixing potential issues promptly.

For cybersecurity enthusiasts and professionals, it's an invaluable tool for gaining insights into system vulnerabilities and sharpening your technical skills.

## Learning Objectives with SMB (Server Message Block)

This project incorporates both Nessus Essentials and SMB security configuration to provide a comprehensive learning experience. Here what you can expect to gain:

### Understand SMB Protocol Security:
- Learn how to enhance the security of the SMB protocol, a common target for attackers.

### Apply Vulnerability Detection to SMB:
- Use Nessus Essentials to scan and identify vulnerabilities related to SMB services.

### Configure Secure SMB Settings:
- Gain hands-on experience using the Group Policy Editor to enable security features like message signing.

### Interpret and Act on Scan Results:
- Learn how to review Nessus scan reports, prioritize risks, and apply effective fixes to vulnerabilities.

### Develop Practical Cybersecurity Skills:
- Combine vulnerability management with system configuration to build your expertise.

---

## Part 1: Installing Nessus Essentials

1. **Go to the Nessus Essentials registration page**  
   [Nessus Essentials Registration](https://www.tenable.com/products/nessus/nessus-essentials)  
2. **Register with a valid email address** to receive a free activation code.

![image](https://github.com/user-attachments/assets/5087e3ab-f957-416b-a682-4ce1f78d072a)

3. **Download and install Nessus Essentials** on your preferred platform:  
   - Windows  
   - macOS  
   - Linux
  
![image](https://github.com/user-attachments/assets/88277df8-9edc-4479-9d68-6f9242d4e14a)
![image](https://github.com/user-attachments/assets/05953c0a-de9d-4b33-b245-befca33aa4e7)
![image](https://github.com/user-attachments/assets/c4af8486-85f2-4065-82b8-480247c6e659)
![image](https://github.com/user-attachments/assets/3e3d0d98-332b-460e-b6d6-001211ef42bd)
![image](https://github.com/user-attachments/assets/f30fbcae-578b-44e8-a446-e59640b90ab0)
![image](https://github.com/user-attachments/assets/7fe91fc5-9479-46d0-a316-f9d6dc9b5c12)
![image](https://github.com/user-attachments/assets/6555c5fd-56aa-4b0d-b86f-a633901c8b11)
![image](https://github.com/user-attachments/assets/acc71d64-7352-4ac3-9ac8-ac6096c992dd)

4. **Activate Nessus Essentials** using the activation code provided.

---

## Part 2: Performing a Host Discovery Scan

### Step 1: Launch Nessus Essentials
After successfully installing and activating **Nessus Tenable Essentials**, launch the application and log in.

### Step 2: Set Up a Host Discovery Scan
1. Navigate to the **New Scan** section.  
2. Select **Host Discovery Scan** from the available scan templates.  
   - This scan is designed to identify active hosts on your network.  
3. Configure the scan by specifying the **IP address or range** of the hosts you want to scan.  
4. Start the scan and wait for it to complete.

### Step 3: Review Scan Results
Once the scan is finished:
- Open the results to view details about the scanned hosts.  
- Nessus Essentials provides a comprehensive list of vulnerabilities detected on each host, categorized by severity.  

This process helps identify potential vulnerabilities in your network, empowering you to take the necessary steps to secure your systems.

![image](https://github.com/user-attachments/assets/14d87ba4-7702-47d4-b0f6-68932f300159)
![image](https://github.com/user-attachments/assets/26861c56-2b80-4aa8-9db5-ebe36c4607cd)

---

## Part 3: Configuring SMB Settings Using Group Policy Editor

### Step 1: Open Group Policy Editor
- Press **Win + R** to open the Run dialog.
- Type `gpedit.msc` and press **Enter** to open the Local Group Policy Editor.

### Step 2: Navigate to SMB Settings
- Navigate to:  
  **Computer Configuration > Administrative Templates > Network > Lanman Workstation**
  
![image](https://github.com/user-attachments/assets/ebd233ea-ef9e-446c-b4f1-0a2f7b678d58)

### Step 3: Configure Message Signing
- Look for the policy named **“Enable Insecure guest logons”**.  
- Double-click on the policy to open its properties.  
- Set it to **“Disabled”**.  
- Click **Apply** and then **OK**.

![image](https://github.com/user-attachments/assets/cc44e229-ed2c-41dd-9bf5-7d3430e5576a)


### Step 4: Apply the Policy
- To ensure the policy is applied immediately:  
  1. Open **Command Prompt** as an administrator.  
  2. Run the following command:  
     ```bash
     gpupdate /force
     ```

---

This project is designed to empower you with practical knowledge, making cybersecurity more accessible and actionable. 



