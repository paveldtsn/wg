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
# V2Ray installer
```bash
{
"server": ["127.0.0.1"],
"mode":"tcp_and_udp",
"server_port":9388,
"local_port":1080,
"password":"password",
"timeout":300,
"method":"xchacha20-ietf-poly1305",
"nameserver":"1.1.1.1",
"no_delay": true,
"fast_open": true,
"reuse_port": true,
"plugin":"/etc/shadowsocks-libev/v2ray-plugin",
"plugin_opts:""server"
}
```
