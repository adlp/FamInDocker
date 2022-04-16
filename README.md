# FamInDocker
Facile Manager dockerized installation

Click'n RUN...or nearly ;P

Basic informations:
  * git clone this repo
  * You have to create an .env file with this :
```
DOCKERROOT=/tmp/            # The root path of your FacileManager Persistent data, might be the repo directory
TZ=Europe/Paris             # Your TimeZone
FMURL=dns.example.lan       # The URL of your FacileManager
DOMAIN=example.lan          # A domain to make your system 
WUITCP=5380                 # The TCP port where your facilemanager will listen in http (so you have to hide him behin a reverse proxy with https)
WUIIP=192.168.0.1           # The IP of the reverse proxy
SSHCLTCP=5322               # The SSH port for the client customer (to push the cfg)
DNSCLTCP=5353               # The DNS tcp port for the client customer (might be 53)
DNSCLUDP=5353               # The DNS udp port for the client customer (might be 53)
# NAMECL=clientdns.example.lan  # The DNS name of client (for simple client)
```

  * create an 'env-fmmaster.env' file with:
```
MYSQL_ROOT_PASSWORD=XXXXXXXXXX
MYSQL_DATABASE=facileManager
MYSQL_USER=facileManager
MYSQL_PASSWORD=YYYYYYYYYY
MYSQL_HOST=mysql
FMMASTER=true
```
  * and finsh by creating an 'env-fmclient.env' file like this:
```
FMMTH=s
FMURL=dns.example.lan       # The URL of your FacileManager
```


TODO:
  - Explain the end of the instal process
