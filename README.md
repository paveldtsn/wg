# WireGuard installer
```bash
curl -O https://raw.githubusercontent.com/paveldtsn/wg/master/wireguard-install.sh
chmod +x wireguard-install.sh
./wireguard-install.sh
```
# ShadowSocks installer
```bash
apt update && apt upgrade -y
apt install shadowsocks-libev -y
vi /etc/shadowsocks-libev/config.json

service shadowsocks-libev restart
service shadowsocks-libev status
systemctl enable shadowsocks-libev

cd /etc/shadowsocks-libev/
wget https://github.com/shadowsocks/v2ray-plugin/releases/download/v1.3.2/v2ray-plugin-linux-amd64-v1.3.2.tar.gz
tar -xvf v2ray-plugin-linux-amd64-v1.3.2.tar.gz
rm v2ray-plugin-linux-amd64-v1.3.2.tar.gz
mv v2ray-plugin_linux_amd64 v2ray-plugin
vi /etc/shadowsocks-libev/config.json

service shadowsocks-libev restart
service shadowsocks-libev status
```
