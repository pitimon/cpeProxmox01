# cpeProxmox
demoLab

## How to Install SSH PowerShell on Windows 
- Step 1. Type PowerShell in the search box, and then right-click the Windows PowerShell and select Run as administrator. Then click on Yes to confirm it
- Step 2.
```
Get-WindowsCapability -Online | ? Name -like 'OpenSSH*'
```
```
Add-WindowsCapability -Online -Name OpenSSH.Client*
```
