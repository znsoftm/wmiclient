# wmiclient
wmi 1.3.16 source code for linux

This is derived from https://askubuntu.com/questions/885407/installing-wmic-on-ubuntu-16-04-lts 

I modified its code to be compatible with new gnutls.

for it, you need to do just as follow: (passwd on ubuntu 18.04)

apt install autoconf gcc libdatetime-perl make build-essential g++ python-dev git clone http:///xxxxx

cd wmi-1.3.16/

vim Samba/source/pidl/pidl :583 (to jump to line 583) remove the word defined before @$pidl :wq

export ZENHOME=/usr make "CPP=gcc -E -ffreestanding" cp Samba/source/bin/wmic /bin
