# laptop-automation

Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux

netsh advfirewall firewall add rule name="Local-Automation-SSH" dir=in action=allow protocol=TCP remoteip=127.0.0.1 localip=127.0.0.1 localport=22
netsh advfirewall firewall add rule name="Local-Automation-WinRM" dir=in action=allow protocol=TCP remoteip=127.0.0.1 localip=127.0.0.1 localport=5986

Restart-Computer

Invoke-WebRequest -Uri https://aka.ms/wsl-ubuntu-1804 -OutFile ~/Ubuntu18.04.appx -UseBasicParsing


