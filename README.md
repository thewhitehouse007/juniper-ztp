# juniper-ztp
Juniper Zero Touch Provisioning

Ubuntu 20

sudo apt update

sudo apt upgrade 

sudo reboot

sudp apt install isc-dhcp-server

yum install vstfpd -y

sudo apt update

#Configure dhcpd for the interface you wish to use - example config in this repo

#Configure vsftpd to be insecure - example config in this repo

systemctl enable dhcpd

systemctl enable vsftpd

systemctl start dhcpd

systemctl start vsftpd

#Place files in /var/ftp/pub

#Configure a cron to do the below or do it manually

chmod -R 777 /var/ftp/pub

chown -R ftp:ftp /var/ftp/pub
