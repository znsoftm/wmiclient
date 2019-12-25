# wmiclient /wmic for linux 
wmi 1.3.16 source code for linux

This is derived from https://askubuntu.com/questions/885407/installing-wmic-on-ubuntu-16-04-lts 

Original package is from  http://www.opsview.com/sites/default/files/wmi-1.3.16.tar_.bz2

I modified its code to be compatible with new gnutls.

For to get a bunch of binary files, you need to do just as follow: (passwd on ubuntu 18.04)

===================================command lines========================

apt install autoconf gcc libdatetime-perl make build-essential g++ python-dev 


git clone https://github.com/znsoftm/wmiclient.git

cd wmi-1.3.16/


export ZENHOME=/usr 
make "CPP=gcc -E -ffreestanding" 
cp Samba/source/bin/wmic /bin
