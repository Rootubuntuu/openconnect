# cisco installer | Ubuntu 18.4


1- 
apt-get update -y && apt-get upgrade -y

2- 
apt install curl

3- 
curl -O https://raw.githubusercontent.com/ciscoiranian/cisco/main/ciscoforiran-installer.sh && chmod +x ciscoforiran-installer.sh

4- 
./ocserv-install.sh

Done!

-----------------------------------------------------------------------------------------------------

# download all Device software

=> https://t.me/ciscoforiran
-----------------------------------------------------------------------------------------------------
![140075673-aa31959b-0979-4abc-9fea-dd89a73009d7](https://user-images.githubusercontent.com/46374084/195152489-1f3f8772-cfa0-4459-bd50-763fc20ddae6.png)


sudo apt install iptables

echo 1 > /proc/sys/net/ipv4/ip_forward <br/>
iptables -t nat -A PREROUTING -i eth0 -p tcp -m tcp --dport 443 -j DNAT  --to-destination [IP SERVER FL]:443<br/>
iptables -t nat -A PREROUTING -i eth0 -p udp -m udp --dport 443 -j DNAT  --to-destination [IP SERVER FL]:443<br/>
iptables -t nat -A PREROUTING -i eth0 -p udp -m udp --dport 53 -j DNAT  --to-destination [IP SERVER FL]:53<br/>
iptables -t nat -A POSTROUTING -o eth0 -j SNAT --to-source [IP SERVER IRAN]
