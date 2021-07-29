### 先安装证书
```
bash /root/.acme.sh/acme.sh --issue -d 域名 --debug --standalone --keylength ec-256 --listen-v6    #“域名”更换掉,cf先变成灰色  

yum install socat #通过80端口生成证书的依赖 #centos7系统
 yum install netcat #centos7系统
 ​
 apt-get install openssl cron socat curl   #debian系统
 apt-get -y install netcat   #debian系统
 
 若安装不上证书，手动改安装acme.sh   
 curl  https://get.acme.sh | sh
 若此命令不成功可先尝试安装：apt-get install socat
 安装好后执行证书安装命令
 ​
 安装成功后执行 source ~/.bashrc 以确保脚本所设置的命令别名生效   
```

### 一键安装xray
``` bash
wget -N --no-check-certificate https://raw.githubusercontent.com/veip007/scripts/master/xray.sh && chmod +x xray.sh && bash xray.sh
```
