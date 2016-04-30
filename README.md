# ShadowSocksX

科学上网

## 服务端

>服务端(这里安装的shadowsocks是python版的):

### 为Debian / Ubuntu 安装shadowsocks服务端:

`$ apt-get install python-pip`

`$ pip install shadowsocks`

### 为CentOs 安装shadowsocks服务端:

`$ yum install python-setuptools`

`$ easy_install pip`

`$ pip install shadowsocks`

### 配置shadowsocks.json:

`$ vim /etc/shadowsocks.json`

>{

>   "server":"0.0.0.0",
   
>   "port":8388,
   
>   "local_address": "127.0.0.1",
   
>   "local_port":1080,
   
>   "password":"199188",
   
>   "timeout":300,
   
>   "method":"aes-256-cfb",
   
>   "fast_open": false,
   
>   "workers": 1
   
>}

### 开启shadowsocks服务:

`$ ssserver -c /etc/shadowsocks.json -d start(stop/restart)`

### 查看log:

`$ tail -n100 -f /var/log/shadowsocks.log`
