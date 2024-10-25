1.下载脚本
支持快捷方式启动，安装完毕后，shell输入【sinian】即可打开脚本，脚本执行路径[/etc/v2ray-agent/install.sh]
```
wget -P /root -N --no-check-certificate "https://raw.githubusercontent.com/sinian-liu/v2ray-agent-2.5.73/master/install.sh" && chmod 700 /root/install.sh && /root/install.sh
```
2.输入【sinian】即可打开脚本
```
sinian
```
3.安装完成后会报错，原因是xray版本不兼容，下载并安装 Xray-core 1.7.5
```
wget -O /etc/v2ray-agent/xray/Xray-linux-64.zip "https://github.com/XTLS/Xray-core/releases/download/v1.7.5/Xray-linux-64.zip"
```
4.解压缩文件，确保安装了 unzip 工具（如果没有，可以先安装）：
```
apt-get install unzip
```
5.然后解压下载的文件：
```
unzip /etc/v2ray-agent/xray/Xray-linux-64.zip -d /etc/v2ray-agent/xray/
```
6.授予执行权限
```
chmod +x /etc/v2ray-agent/xray/xray
```
7.配置和重启服务
```
systemctl restart xray
```

