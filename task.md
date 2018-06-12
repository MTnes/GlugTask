mkdir music touch song{1..10}.mp3 mv song*.mp3 ./music ln -s music audio

sudo -s groupadd sysadmin useradd -m bob -p linux123 useradd -m rob -p linux123 groupadd manager useradd -m max -p linux123 usermod -g sysadmin rob usermod -g sysadmin bob usermod -g sysadmin max usermod -a -G manager rob usermod -a -G manager bob

vim /etc/passwd change max❌1003:1005::/home/bin/bash to max❌1003:1005::/home/bin/false sudo change -E 'date -d "30 days" +"%Y-%m-%d"' max change -d 0 bob

mkdir /home/manager chgrp manager /home/manager chmod -R 2770 /home/manager

useradd -u 4223 gabriel

mkdir /tmp/var tar -cvf /tmp/var/archive.tar.bz2 /etc/hosts

grep udp /etc/service > udp_services.txt

top shift+f then s for sorting

echo 'alias stat="/bin/uptime"' >> ~/.zshrc source ~/.zshrc

vim aarck.txt :i for insert :shift+zz to save and exit :x to delete :q exit without saving

firewall-cmd --get-default-zone firewall-cmd --set-default-zone=dmz firewall-cmd --get-zones > zones.txt

firewall-cmd –zone=public –add-port=25/tcp –permanent firewall-cmd --list-ports>zones.txt

iptables -A PREROUTING -t nat -i eth0 -p tcp --dport 80 -j REDIRECT --to-port 8080
