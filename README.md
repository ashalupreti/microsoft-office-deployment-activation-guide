# Microsoft Office 2021 / 2019 / LTSC 2024 Deployment & Activation Guide

Complete step-by-step guide for deploying, installing, configuring, and activating Microsoft Office using the Office Deployment Tool (ODT).

Supports:

- Microsoft Office 2016
- Microsoft Office 2019 Pro Plus
- Microsoft Office LTSC 2021
- Microsoft Office LTSC 2024
- Volume License Installation
- Office Deployment Tool (ODT)
- KMS Activation
- Enterprise Office Deployment

---

<p align="center">
  <img src="https://img.shields.io/badge/Microsoft%20Office-Deployment-blue?style=for-the-badge&logo=microsoftoffice">
  <img src="https://img.shields.io/badge/Office-LTSC%202024-green?style=for-the-badge">
  <img src="https://img.shields.io/badge/Windows-Compatible-success?style=for-the-badge&logo=windows">
  <img src="https://img.shields.io/badge/License-Educational-orange?style=for-the-badge">
</p>
![Platform](https://img.shields.io/badge/Platform-Windows%2010%2F11-blue?style=for-the-badge&logo=windows)

## Official Microsoft Resources

### Office Deployment Documentation
https://learn.microsoft.com/en-us/deployoffice/office2019/deploy

---

# Installation Guide

## Step 1 — Download Office Deployment Tool (ODT)

Download the official Office Deployment Tool from Microsoft https://www.microsoft.com/en-us/download/details.aspx?id=49117

After downloading, extract it into a folder on your system:

``` D:\OfficeSetup ```

This folder will contain setup.exe, which is used for downloading and installing Office.

---

## Step 2 — Create Configuration File (XML)

Go to the official Office Configuration Tool:

https://config.office.com/

Here you can:
- Select Office version
- Choose apps (Word, Excel, PowerPoint, etc.)
- Select language
- Choose architecture (32-bit / 64-bit)

After configuration, export and save the file as:

configuration.xml

Place this file inside the same folder:

``` D:\OfficeSetup ```

---

## Step 3 — Download Office Files

Open Command Prompt as Administrator and run:

```
cd D:\OfficeSetup setup.exe /download configuration.xml
```

---

## Step 4 — Install Office

Run:

```
setup.exe /configure configuration.xml
```

---

## step 5— Install Office 2021 Volume License

Run:

```
for /f %x in ('dir /b ..\root\Licenses16\ProPlus2021VL_KMS*.xrm-ms') do cscript ospp.vbs /inslic:"..\root\Licenses16\%x"

```

---

# Open Command Prompt as Administrator

Change directory:

```
cd C:\Program Files\Microsoft Office\Office16
```

# Activation (Choose Your Office Version)

### For example

```
cscript ospp.vbs /inpkey:FXYTK-NJJ8C-GB6DW-3DYQT-6F7TH  
cscript ospp.vbs /unpkey:BTDRB >nul  
cscript ospp.vbs /unpkey:KHGM9 >nul  
cscript ospp.vbs /unpkey:CPQVG >nul  
cscript ospp.vbs /sethst:kms8.msguides.com  
cscript ospp.vbs /setprt:1688  
cscript ospp.vbs /act
```

---

## Office 2016

```
cscript ospp.vbs /inpkey:XQNVK-8JYDB-WJ9W3-Y8YR-WFG99  
cscript ospp.vbs /inpkey:BTDRB >nul  
cscript ospp.vbs /inpkey:KHGM9 >nul  
cscript ospp.vbs /inpkey:CPQVG >nul  
cscript ospp.vbs /sethst:kms8.msguides.com  
cscript ospp.vbs /setprt:1688  
cscript ospp.vbs /act
```


---

## Office Pro Plus 2019

```
cscript ospp.vbs /inpkey:NMMKJ-6RK4F-KMJVX-8D9MJ-6MWKP  
cscript ospp.vbs /inpkey:BTDRB >nul  
cscript ospp.vbs /inpkey:KHGM9 >nul  
cscript ospp.vbs /inpkey:CPQVG >nul    
cscript ospp.vbs /sethst:kms8.msguides.com  
cscript ospp.vbs /setprt:1688  
cscript ospp.vbs /act
```

---

## Office LTSC 2021

```
cscript ospp.vbs /inpkey:FXYTK-NJJ8C-GB6DW-3DYQT-6F7TH  
cscript ospp.vbs /unpkey:BTDRB >nul  
cscript ospp.vbs /unpkey:KHGM9 >nul  
cscript ospp.vbs /unpkey:CPQVG >nul  
cscript ospp.vbs /sethst:kms8.msguides.com  
cscript ospp.vbs /setprt:1688  
cscript ospp.vbs /act
```

---

## Office LTSC 2024

```
cscript ospp.vbs /inpkey:Y63J7-9RNDJ-GD3BV-BDKBP-HH966  
cscript ospp.vbs /unpkey:BTDRB >nul  
cscript ospp.vbs /unpkey:KHGM9 >nul  
cscript ospp.vbs /unpkey:CPQVG >nul  
cscript ospp.vbs /sethst:kms8.msguides.com  
cscript ospp.vbs /setprt:1688  
cscript ospp.vbs /act
```

---

# Useful Office Commands

## Activate Microsoft Office

cscript ospp.vbs /act 

## Remove Existing Product Key

cscript ospp.vbs /unpkey:BTDRB 

## Check Office Activation Status

cscript ospp.vbs /dstatus 

---

# Troubleshooting

## Office Activation Failed

- Ensure internet connection is active
- Run Command Prompt as Administrator
- Verify Office version compatibility
- Recheck KMS server configuration

## Cannot Find ospp.vbs

Ensure Office is installed in:

```C:\Program Files\Microsoft Office\Office16```

---

# FAQ

## What is Office Deployment Tool?

Office Deployment Tool (ODT) is Microsoft’s official utility for downloading and deploying Office products.

## Does this support Office LTSC 2024?

Yes, this guide supports Office LTSC 2024 volume license deployment and activation.

## Can I customize Office apps during installation?

Yes. Use the Microsoft Office Customization Tool to create your own XML configuration.

---

# Disclaimer

This repository is intended for educational, deployment, and research purposes only. Users are responsible for complying with Microsoft licensing policies and software agreements.

---

# Star This Repository

If this repository helped you, consider giving it a star to support the project.
