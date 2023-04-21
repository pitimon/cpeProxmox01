# cpeProxmox
demoLab

## How to Install SSH PowerShell on Windows 
[https://learn.microsoft.com/en-us/windows-server/administration/openssh/openssh_install_firstuse?tabs=powershell]
- Step 1. Type PowerShell in the search box, and then right-click the Windows PowerShell and select Run as administrator. Then click on Yes to confirm it
- Step 2.
```
Get-WindowsCapability -Online | ? Name -like 'OpenSSH*'
```
```
Add-WindowsCapability -Online -Name OpenSSH.Client*
```
## Prepare Guest
```
apt update
apt install git
```
- Request step
```

```
## Docker Engine install
[https://docs.docker.com/engine/install/ubuntu/]
```
sudo apt-get update
sudo apt-get install \
    ca-certificates \
    curl \
    gnupg

sudo install -m 0755 -d /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
sudo chmod a+r /etc/apt/keyrings/docker.gpg

echo \
  "deb [arch="$(dpkg --print-architecture)" signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  "$(. /etc/os-release && echo "$VERSION_CODENAME")" stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

sudo apt-get update

sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin docker-compose -y
```
