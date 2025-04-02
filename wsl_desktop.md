from https://www.bilibili.com/video/BV1qbQGYPEg7/?spm_id_from=333.1391.0.0&vd_source=ee200f7e09eb8dbc8631c991d8917853

* sudo apt install xfce4 xfce4-goodies
  
* sudo apt install xrdp

* sudo cp /etc/xrdp/xrdp.ini /etc/xrdp/xrdp.ini.bak

* sudo sed -i 's/3389/3390/g' /etc/xrdp/xrdp.ini

* sudo sed -i 's/max_bpp=32/#max_bpp=32\nmax_bpp=128/g' /etc/xrdp/xrdp.ini

* sudo /etc/init.d/xrdp start

* sudo vim /etc/xrdp/startwm.sh
```注释掉下面内容
test -x /etc/X11/Xsession && exec /etc/X11/Xsession
exec /bin/sh /etc/X11/Xsession
```
```添加下面内容跟
startxfce4
```

* sudo /etc/init.d/xrdp start

* windows remote desktop connection
```
localhost:3390
```
* 
