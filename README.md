# FamInDocker
Facile Manager dockerized installation

Click'n RUN...or nearly ;P

Basic informations:
  * git clone this repo
  * You have to create an .env file with this :
```
#### Base Configuration
DOCTAG=03                   # Let you choose the image tag
DOCKERROOT=/tmp/            # The root path of your FacileManager Persistent data, might be the repo directory
TZ=Europe/Paris             # Your TimeZone
FMURL=dns.example.lan       # The URL of your FacileManager
DOMAIN=example.lan          # A domain to make your system 
#### Web User Interface Configuration
WUILIP=0.0.0.0              # IP where the WUI have to be binded
WUITCP=5380                 # The TCP port where your facilemanager will listen in http (so you have to hide him behin a reverse proxy with https)
WUIIP=192.168.0.1           # The IP of the reverse proxy
#### FacileManager Client Configuration
# NAMECOCL=clientdns        # The container name on the host
SSHLIP=0.0.0.0              # IP where the SSH have to be binded
SSHCLTCP=5322               # The SSH port for the client customer (to push the cfg)
DNSLIP=0.0.0.0              # IP where the DNS have to be binded
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
# NAMESERVERNAME=fmdns00.dns.example.lan   # If you wish that your container use another container to solve :)
# HOSTTOFILE=h3:192.168.42.56,h4:192.168.68.200 # Add some line in your /etc/hosts, without modify docker-compose ;)
```
  * and finsh by creating an 'env-fmclient.env' file like this:
```
FMMTH=s
FMURL=dns.example.lan       # The URL of your FacileManager
# NAMESERVERNAME=fmdns00.dns.example.lan   # If you wish that your container use another container to solve :)
# HOSTTOFILE=h1:192.168.2.56,h2:192.168.67.254  # Add some line in your /etc/hosts, without modify docker-compose ;)
```


TODO:
  - Explain the end of the instal process
