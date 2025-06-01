# Setup-and-Use-a-Firewall-on-Windows-Linux
Windows Firewall (Windows Defender Firewall)
Check Firewall Status
Open Control Panel → System and Security → Windows Defender Firewall
Make sure it's turned on for both Private and Public networks.

Allow or Block a Program
Go to:
Control Panel → Windows Defender Firewall → Allow an app or feature through Windows Defender Firewall
Click Change settings → Tick or untick programs to allow/block.

Create Inbound/Outbound Rules
Open Windows Defender Firewall with Advanced Security (search in Start).
Select Inbound Rules or Outbound Rules → Click New Rule.
Choose:
Program: Block a specific .exe file.
Port: Block or allow a port (e.g., TCP 80).
Define the rule → Name it → Finish.

Block a Port (Example: Block Port 21 - FTP)
Go to Advanced Firewall Settings → Inbound Rules → New Rule.
Choose Port → Enter 21 → Block the connection → Name it.

Linux Firewall: UFW (Uncomplicated Firewall)
Install UFW
Debian/Ubuntu:
sudo apt install ufw

Enable UFW
sudo ufw enable

Check Status
sudo ufw status verbose

Allow or Deny Services/Ports
Allow SSH (port 22):
sudo ufw allow ssh

Allow a specific port (e.g., 80 for HTTP):
sudo ufw allow 80

Deny FTP (port 21):
sudo ufw deny 21

Block a specific IP:
sudo ufw deny from 192.168.1.100

Delete a Rule
sudo ufw delete allow 80

Disable the Firewall (when needed)
sudo ufw disable






