# Set up a dns server

to set up a dns server you should have dnsmasq installed

```bash
sudo apt install dnsmasq
```


The you need to add the following config to /etc/dnsmasq.conf
**Replace enx00e04c680390 with your lan interface**

```bash
interface=enx00e04c680390
listen-address=192.168.100.250
bind-interfaces
address=/www.redesfinal.com/192.168.100.250

```


remember to edit it as **root**

The reestart the dnsmasq service


```bash
sudo systemctl restart dnsmasq 
```

## Cliend dns

Finally add the dns server to /etc/resolv.conf
***Change the ip with the dns server
```bash
nameserver 127.0.0.1
```