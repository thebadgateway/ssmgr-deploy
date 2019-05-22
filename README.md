This script is a one-click deployment script for the shadowsocks-manager server.

### Version introduction

server uses is shadowsocks-libev[View the latest version](https://github.com/shadowsocks/shadowsocks-libev/releases)

server uses is shadowsocks-manager[View the latest version](https://github.com/shadowsocks/shadowsocks-manager)


### installation method

Install wget
```
# centos
yum -y install wget

# Ubuntu
apt-get -y install wget
```

Download script
```
rm -rf ./install.sh ./shadowsocks-manager.log
wget --no-check-certificate https://raw.githubusercontent.com/quniu/ssmgr-deploy/master/install.sh
chmod +x install.sh
./install.sh 2>&1 | tee shadowsocks-manager.log
```


### Features
- Install the shadowsocks-manager service
- Set a fixed time to automatically restart (select the last item)



### Installation Notes
The log is under `/root/`

The script is under `/root/`

shadowsocks-manager Installation directory at`/usr/local/`



### Listening port

Server enabled port `6001`

The client enables port `6002` (can also be defined by itself)

The client enables the password `you need to fill it out yourself.



### View the shadowsocks service

After the default installation is successful, the ss service will be started automatically, and the restart will automatically start the ss service.
```
# status stop start restart
/etc/init.d/shadowsocks-manager status
```

This script is purely for learning, please do not use it for commercial activities.
