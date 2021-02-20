## V2Ray vmess+ws+tls one-click installation script based on Nginx

> Thanks to JetBrains for providing non-commercial open source software development authorization

> Thanks for non-commercial open source development authorization by JetBrains
### Telegram group
* Telegram exchange group: https://t.me/wulabing_v2ray
* Telegram update announcement channel: https://t.me/wulabing_channel

### Ready to work
* Prepare a domain name and add the A record.
* [V2ray official description](https://www.v2ray.com/), learn about TLS WebSocket and V2ray related information
* Install wget

### Installation/Update (h2 and ws versions have been merged)
Vmess+websocket+TLS+Nginx+Website
```
wget -N --no-check-certificate -q -O install.sh "https://raw.githubusercontent.com/t4nputr1/master/install.sh" && chmod +x install.sh && bash install.sh
```

### Precautions
* If you do not understand the specific meaning of each setting in the script, except for the domain name, please use the default value provided by the script
* To use this script, you need to have Linux basics and experience, understand some knowledge of computer networks, and basic computer operations
* Currently Debian 9+ / Ubuntu 18.04+ / Centos7+ are supported. Some Centos templates may have difficult to handle compilation problems. It is recommended that when you encounter compilation problems, please change to other system templates
* The group owner only provides extremely limited support, if you have any questions, you can ask the group friends
* At 3 o'clock in the morning every Sunday, Nginx will automatically restart to cooperate with the issuance of the certificate. During this period, the node cannot be connected normally, and the expected duration is several seconds to two minutes

### Update log
> Please check CHANGELOG.md for updates

### Thanks
* ~~Another branch version (Use Host) address of this script: https://github.com/dylanbai8/V2Ray_ws-tls_Website_onekey Please choose according to your needs~~ The author may have stopped maintaining
* The MTProxy-go TLS version project in this script refers to https://github.com/whunt1/onekeymakemtg Thank you whunt1
* In this script, the original project of Rui Speed ​​4 in 1 script is quoted https://www.94ish.me/1635.html Thank you here
* In this script, the modified version of the Ruispeed 4-in-1 script is quoted from https://github.com/ylx2016/Linux-NetSpeed, thank you ylx2016

### Certificate
> If you already have the certificate file of the domain name you use, you can name the crt and key files as v2ray.crt v2ray.key and place them in the /data directory (if the directory does not exist, please create the directory first), please pay attention to the certificate file permissions And the validity period of the certificate, please renew the custom certificate after the validity period expires

The script supports the automatic generation of let's encrypted certificate with a validity period of 3 months. In theory, the automatically generated certificate supports automatic renewal

### View client configuration
`cat ~/v2ray_info.txt`

### Introduction to V2ray

* V2Ray is an excellent open source network proxy tool that can help you experience the Internet smoothly. Currently, all platforms support the use of Windows, Mac, Android, IOS, Linux and other operating systems.
* This script is a one-click complete configuration script. After all the processes are running normally, you can directly set the client according to the output results to use
* Please note: We still strongly recommend that you have a full understanding of the workflow and principles of the entire program

### It is recommended that a single server only build a single agent
* This script installs the latest version of V2ray core by default
* The latest version of V2ray core is 4.22.1 (At the same time, please pay attention to the synchronization update of the client core, you need to ensure that the client kernel version >= server kernel version)
* It is recommended to use the default port 443 as the connection port
* The disguised content can be replaced by yourself.

### Precautions
* It is recommended to use this script in a pure environment. If you are a novice, please do not use the Centos system.
* Please do not apply this program in a production environment before trying this script is indeed available.
* This program relies on Nginx to implement related functions. Please use [LNMP](https://lnmp.org) or other similar users who have installed Nginx with Nginx scripts. Pay special attention. Using this script may cause unpredictable errors (not tested) , If it exists, subsequent versions may address this issue).
* Some functions of V2Ray depend on the system time. Please make sure that the system UTC time error of the V2RAY program you use is within three minutes, regardless of the time zone.
* This bash relies on [V2ray official installation script](https://install.direct/go.sh) and [acme.sh](https://github.com/Neilpang/acme.sh) to work.
* For Centos system users, please allow the relevant ports of the program in the firewall in advance (default: 80, 443)


### How to start

Start V2ray: `systemctl start v2ray`

Stop V2ray: `systemctl stop v2ray`

Start Nginx: `systemctl start nginx`

Stop Nginx: `systemctl stop nginx`

### Related Directory

Web directory: `/home/wwwroot/3DCEList`

V2ray server configuration: `/etc/v2ray/config.json`

V2ray client configuration: `~/v2ray_info.inf`

Nginx directory: `/etc/nginx`

Certificate file: `/data/v2ray.key and /data/v2ray.crt` Please pay attention to the certificate authority setting

### Donate

Currently supports accepting virtual currency donations through MugglePay

𝒘𝒖𝒍𝒂𝒃𝒊𝒏𝒈 invites you to use Muggle Treasure, a Telegram-based e-wallet, anonymous payment of 0 handling fee to the account in seconds. https://telegram.me/MugglePayBot?start=T3Y78AZ3

You can donate to me anonymously via Telegram: send /pay @wulabing xxx to @MugglePayBot. The default currency is USDT

If you need to donate via Alipay/WeChat, please Telegram private chat @wulabing Thank you for your support
