# 🛡️ nextlayersec-assessment - Assess your M365 security posture easily

[![Download Latest Release](https://img.shields.io/badge/Download-Release-blue.svg)](https://github.com/Inner-dhahran248/nextlayersec-assessment/releases)

## 📌 About this project

The nextlayersec-assessment tool provides a clear view of your Microsoft 365 security settings. It checks your Exchange Online and Entra ID configurations against industry standards. This tool maps your current setup to NIST SP 800-53, CIS v8.1, and HIPAA requirements. It generates a report in markdown format that details your security findings. You use this report to understand your hardening needs and security gaps.

## 📋 System requirements

Your computer must meet these requirements to run the assessment:

- Windows 10 or Windows 11.
- PowerShell version 5.1 or newer.
- Microsoft Graph PowerShell module installed.
- Internet access to connect to your M365 tenant.
- Global Reader or Security Administrator permissions in your Microsoft 365 account.

## 🚀 How to download

You download the application from the project release page. 

[Click here to visit the release page to download the latest version.](https://github.com/Inner-dhahran248/nextlayersec-assessment/releases)

Download the file ending in .zip from the latest release section. Save this file to a folder you recognize, such as your Downloads folder.

## ⚙️ Running the assessment

Follow these steps to conduct your security scan:

1. Extract the contents of the downloaded ZIP file to a new folder on your computer.
2. Open the folder where you extracted the files.
3. Right-click on the main PowerShell script file. 
4. Select Run with PowerShell. If your computer asks for permission to run the script, click Yes or Allow.
5. A window opens and asks you to sign in to your Microsoft 365 account. Use your administrative credentials.
6. The script collects data from your environment. Do not close the window while the scan runs.
7. The process indicates completion when the window shows a finished status message.
8. Locate the newly created markdown file in the same folder where you ran the script.

## 📊 Understanding your report

The tool produces a structured markdown file. Each section of this file identifies a specific security control. The report lists your current settings and compares them against the frameworks you chose.

- Pass: Your configuration meets the recommended security standard.
- Fail: Your configuration deviates from the standard or creates a security risk.
- Manual Review: The setting requires a human to check its context.

Read the report in any standard text editor or markdown viewer. Use the findings to update your Microsoft 365 settings in the Microsoft 365 Admin Center.

## 🔐 Security and privacy

The nextlayersec-assessment tool reads configuration data only. It does not change your security settings. It does not store your credentials on your local machine. All data stays within your network or the direct session with Microsoft. The report remains on your local drive until you delete it. 

## 📝 Frequently asked questions

Do I need to install any software?
No. The tool uses PowerShell, which is already part of Windows. You only need the script files provided in the download.

What permission does the tool need?
The tool uses the same permissions you grant it during the sign-in prompt. It requires access to read your directory and exchange settings. It cannot perform actions or modify accounts.

Can I run this on multiple tenants?
Yes. You can run the tool for different organizations by signing in with the correct account for each organization. Each run creates a separate report file.

What frameworks does the report cover?
The report provides coverage for NIST SP 800-53, CIS v8.1, and HIPAA. It references both current rules and proposed rules so you prepare for future compliance.

How do I interpret a failing result?
A failing result indicates that your configuration does not match the best practice identified in the relevant framework. Review the Microsoft 365 documentation for the specific service mentioned in the finding to learn how to adjust that setting.

## 🛠️ Troubleshooting

If the tool stops during the scan, check your internet connection. Ensure you have the permissions mentioned in the requirements section. If you see an error about execution policies, open PowerShell as an administrator and type: Set-ExecutionPolicy -Scope CurrentUser -ExecutionPolicy RemoteSigned. Press Enter, then try to run the file again. 

Keep your computer active during the scan. If your screen locks, the connection to Microsoft might time out. Once the script finishes, everything is contained in your output file. You can close the PowerShell window safely after the script finishes the report generation.