# juniper-ztp
Juniper Zero Touch Provisioning

**Ubuntu 20.00**
```bash
sudo apt update

sudo apt upgrade 

sudo reboot

sudo apt install isc-dhcp-server

yum install vstfpd -y

sudo apt update
```

#Configure dhcpd for the interface you wish to use in '/etc/default/isc-dhcp-server' 
    DHCPDv4_CONF=/etc/dhcp/dhcpd.conf
    INTERFACESv4="ens160"

#Configure vsftpd to be insecure - example config in this repo
```bash
systemctl enable isc-dhcp-server

systemctl enable vsftpd

systemctl start isc-dhcp-server

systemctl start vsftpd
```
#Place files in /var/ftp/pub

#Configure a cron to do the below or do it manually

    chmod -R 777 /var/ftp/pub

    chown -R ftp:ftp /var/ftp/pub
