# deepin-scripts
- https://packages.debian.org/bullseye/amd64/libffi7/download

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

************************************************************************************
add repositorio debian
Adicionando Repositório PPA no Deepin ou Debian



https://blog.anantshri.info/howto-add-ppa-in-debian/

https://anantshri.info/uploads/2010/09/add-apt-repository.sh.txt

#!/bin/bash
if [ $# -eq 1 ]
NM=`uname -a && date`
NAME=`echo $NM | md5sum | cut -f1 -d" "`
then
	ppa_name=`echo "$1" | cut -d":" -f2 -s`
	if [ -z "$ppa_name" ]
	then
		echo "PPA name not found"
		echo "Utility to add PPA repositories in your debian machine"
		echo "$0 ppa:user/ppa-name"
	else
		echo "$ppa_name"
		echo "deb http://ppa.launchpad.net/$ppa_name/ubuntu lucid main" >> /etc/apt/sources.list
		apt-get update >> /dev/null 2> /tmp/${NAME}_apt_add_key.txt
		key=`cat /tmp/${NAME}_apt_add_key.txt | cut -d":" -f6 | cut -d" " -f3`
		apt-key adv --keyserver keyserver.ubuntu.com --recv-keys $key
		rm -rf /tmp/${NAME}_apt_add_key.txt
	fi
else
	echo "Utility to add PPA repositories in your debian machine"
	echo "$0 ppa:user/ppa-name"
fi

—-------------------------------------

Steps to install this.
Download file
$ wget https://blog.anantshri.info/content/uploads/2010/09/add-apt-repository.sh.txt
2.  Save this file in /usr/sbin/
$ cp add-apt-repository.sh.txt /usr/sbin/add-apt-repository
3.  Change permissions to execute
$ chmod o+x /usr/sbin/add-apt-repository
4.  Change ownership to root
$chown root:root /usr/sbin/add-apt-repository
5.  Now when ever you need to execute command type
$ sudo add-apt-repository ppa:ppa-name
Opening this script to larger audience so that we can crowdsource efforts if someone likes it.
hope this can help someone

http://agoracomlinux.blogspot.com/2016/06/adicionando-ppa-no-debian.html

https://samthngs.wordpress.com/2017/11/29/adicionando-repositorio-ppa-no-deepin-ou-debian/

sudo add-apt-repository ppa:mattrose/terminator
sudo apt-get update
sudo apt install terminator

—------------------------***************************************************
install docker deepin

https://gist.github.com/madkoding/3f9b02c431de5d748dfde6957b8b85ff

sudo systemctl start docker
sudo systemctl enable docker
sudo groupadd docker
sudo usermod -aG docker $USER

