# Ubuntu için SOCKS5 Proxy Kurulum Scripti

Bu depo, Ubuntu sistemi üzerinde SOCKS5 proxy sunucusu kurmanıza yardımcı olan bir script içermektedir. Sunucu, `dante-server` yazılımını kullanır ve kullanıcı adı/şifre ile kimlik doğrulamasını destekler.

## 🧰 Gereksinimler

- Ubuntu işletim sistemi (Script Ubuntu 20.04 üzerinde test edilmiştir, diğer sürümlerde de çalışması beklenir).
- `sudo` yetkilerine sahip bir kullanıcı hesabı.

## ⚙️ Kurulum

Scripti çalıştırmak için aşağıdaki komutları terminale yazın:

```bash
wget https://raw.githubusercontent.com/g0khanbey/socks5/main/socks5.sh
sudo bash socks5.sh

sudo systemctl status danted


```

You'll be prompted for a username and password. These will be the credentials for the SOCKS5 proxy.


## Testing the Proxy
Proxy’nin düzgün çalışıp çalışmadığını test etmek için Windows ortamında curl komutunu kullanabilirsiniz.

Eğer curl yüklü değilse aşağıdaki komutla yükleyebilirsiniz:
```bash
apt-get install curl
```

test baglantisi:
```
curl -x socks5://username:password@proxy_server_ip:1080 https://ifconfig.me
```
