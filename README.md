# CyberPatriots-Linux-Things

#!/bin/bash

#firewall-stuff
sudo ufw reset
sleep 2
sudo ufw enable
sleep 2
sudo ufw default deny incoming
sleep 2
sudo ufw default allow outgoing
sleep 2
sudo ufw status
sleep 2

#install-firefox
sudo apt install firefox
sleep 2

#disable-guest-account
sudo echo "allow-guest=false" >> 50-ubuntu.conf
sleep 2

#pam-file-stuff
sudo apt install libpam-cracklib
sleep 1
cd /etc/pam.d
sleep 1
sed -i 's/pam_pwquality.so retry=3/pam_cracklib.so retry=3 minlen=8 difok=3 ucredit=-1 lcredit=-1 ocre$/' common-password
sleep 1
sed -i 's/yescrypt/sha512/' common-password
sleep 2

#delete-bad-apps
apt remove john-the-ripper
sleep 1
apt remove hydra
sleep 1
apt remove nmap
sleep 1
apt remove metasploit
sleep 1
apt remove wireshark
sleep 1
apt remove john-netcat 
sleep 1
apt remove bind9 
sleep 1
apt remove telnet
sleep 1
apt remove iodine 
sleep 1
apt remove kismet
sleep 1
apt remove medusa 
sleep 1
apt remove rsh-server 
sleep 1
apt remove fcrackzip 
sleep 1
apt remove ayttm 
sleep 1
apt remove empathy 
sleep 1
apt remove nikto 
sleep 1
apt remove logkeys
sleep 1
apt remove nfs-kernel-server 
sleep 1
apt remove vino 
sleep 1
apt remove tightvncserver 
sleep 1
apt remove rdesktop 
sleep 1
apt remove remmina 
sleep 1
apt remove vinagre 
sleep 1
apt remove bettercap 
sleep 1
apt remove knocker 
sleep 1
apt remove openarena-server 
sleep 1
apt remove minetest 
sleep 1
apt remove minetest-server 
sleep 1
apt remove zenmap
sleep 1
apt remove Tcpdump
sleep 1
apt remove Reaver
sleep 1
apt remove Netcat
sleep 1
apt remove o airbase-ng
sleep 1
apt remove o aircrack-ng
sleep 1
apt remove o airdecap-ng
sleep 1
apt remove o airdecloak-ng
sleep 1
apt remove o airdrop-ng
sleep 1
apt remove o aireplay-ng
sleep 1
apt remove o airgraph-ng
sleep 1
apt remove o airmon-ng
sleep 1
apt remove o airodump-ng
sleep 1
apt remove o airolib-ng
sleep 1
apt remove o airserv-ng
sleep 1
apt remove o airtun-ng
sleep 1
apt remove o besside-ng
sleep 1
apt remove o dcrack
sleep 1
apt remove o easside-ng
sleep 1
apt remove o packetforge-ng
sleep 1
apt remove o tkiptun-ng
sleep 1
apt remove o wesside-ng
sleep 1

apt-get install auditd
sleep 1
auditctl –e 1
sleep 2

#END
