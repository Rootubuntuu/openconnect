# OpenConnect
The environment used in the tutorial ubuntu 18.4 & 20.4
Install with one click

1- Update operating system packages 

```
apt-get update -y && apt-get upgrade -y
```
2- install curl 

```
apt install curl
```
3- Download required services

```
curl -O https://raw.githubusercontent.com/Rootubuntuu/openconnect/main/openconnect-installer.sh && chmod +x openconnect-installer.sh
```
4- Installation

```
./openconnect-installer.sh
```
______________________________________________________________________________________________________________________________________________
# Limit the number of identical clients

```
nano /etc/ocserv/ocserv.conf
```

#After each change in the ocserv.conf file, run the following commands to apply

STOP
```
service ocserv stop
```

START
```
service ocserv start
```

______________________________________________________________________________________________________________________________________________
# Configuration for MacBook and iPhone

Install Apache or Nginx: 
```
sudo apt-get install apache2
```
OR

```
sudo apt-get install nginx
```

CMD COPY CA-CERT.PEM

```
sudo cp /certificates/ca-cert.pem /var/www/html
```
