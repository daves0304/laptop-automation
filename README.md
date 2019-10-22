# laptop-automation

netsh advfirewall firewall add rule name="Local-Automation-SSH" dir=in action=allow protocol=TCP remoteip=127.0.0.1 localip=127.0.0.1 localport=22

netsh advfirewall firewall add rule name="Local-Automation-WinRM" dir=in action=allow protocol=TCP remoteip=127.0.0.1 localip=127.0.0.1 localport=5986

Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux

Restart-Computer


  
Invoke-WebRequest -Uri https://aka.ms/wsl-ubuntu-1804 -OutFile ~/Ubuntu18.04.appx -UseBasicParsing

~/Ubuntu18.04.appx



sudo apt update

sudo DEBIAN_FRONTEND=noninteractive apt upgrade -y

sudo apt install -y python-pip python3-pip

pip3 install ansible

source .bashrc

source .profile
