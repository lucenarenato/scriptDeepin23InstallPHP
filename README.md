# deepin-scripts

## RUN

```sh
sudo chmod -R 777 deepin-scripts-php8.2-installer.sh
sudo chmod -R 777 version_php.sh
sudo ./deepin-scripts-php8.2-installer.sh
sudo ./version_php.sh
```

## Outras informacoes

- https://packages.debian.org/bullseye/amd64/libffi7/download

```sh
sudo apt policy php
sudo apt install libdav1d4
sudo apt install libdav1d5
sudo apt --fix-broken install
sudo apt autoremove
sudo apt install libffi8
sudo apt install php8.2-fpm
wget http://ftp.br.debian.org/debian/pool/main/libf/libffi/libffi7_3.3-6_amd64.deb
sudo dpkg -i libffi7_3.3-6_amd64.deb
sudo apt install -f
```

> Linux renato-HP 6.9.6-amd64-desktop-rolling #23.01.01.02 SMP PREEMPT_DYNAMIC Tue Jul 23 12:20:02 CST 2024 x86_64 GNU/Linux

```sh
cat /etc/os-version
[Version]
SystemName=Deepin
SystemName[zh_CN]=深度操作系统
ProductType=Desktop
ProductType[zh_CN]=桌面
EditionName=Community
EditionName[en_US]=Community
EditionName[zh_CN]=社区版
MajorVersion=23
MinorVersion=23
OsBuild=31038.101
```
