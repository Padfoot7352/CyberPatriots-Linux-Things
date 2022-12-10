# CyberPatriots-Linux-Things

#!/bin/bash

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

#END
