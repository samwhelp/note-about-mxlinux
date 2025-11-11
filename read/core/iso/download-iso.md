---
title: Download ISO
nav_order: 1000
has_children: false
parent: ISO
---


# Download ISO




## MX 25

* MxLinux / [News](https://mxlinux.org/mx-linux-blog/) / [MX 25 “Infinity” isos now available!](https://mxlinux.org/blog/mx-25-infinity-isos-now-available/)




## 下載腳本

* [下載腳本](https://github.com/samwhelp/mxlinux-adjustment/tree/main/core/iso/boot-iso/boot-iso-by-grub/demo-boot-mxlinux-iso)




## 下載點

> 可以到下面網址，尋找下載點。

* MxLinux / [Download](https://mxlinux.org/download-links/) / [Mirrors](https://rsync-mxlinux.org/mirmon/index.html)




## 下載方式


### iso-download.txt

先產生一個檔案「`iso-download.txt`」，內容如下

```
https://sourceforge.net/projects/mx-linux/files/Final/Xfce/MX-25_Xfce_x64.iso
https://sourceforge.net/projects/mx-linux/files/Final/KDE/MX-25_KDE_x64.iso
https://sourceforge.net/projects/mx-linux/files/Final/Fluxbox/MX-25_fluxbox_x64.iso




https://sourceforge.net/projects/mx-linux/files/Final/Xfce/MX-25_Xfce_x64.iso.sig
https://sourceforge.net/projects/mx-linux/files/Final/Xfce/MX-25_Xfce_x64.iso.sha256
https://sourceforge.net/projects/mx-linux/files/Final/KDE/MX-25_KDE_x64.iso.sig
https://sourceforge.net/projects/mx-linux/files/Final/KDE/MX-25_KDE_x64.iso.sha256
https://sourceforge.net/projects/mx-linux/files/Final/Fluxbox/MX-25_fluxbox_x64.iso.sig
https://sourceforge.net/projects/mx-linux/files/Final/Fluxbox/MX-25_fluxbox_x64.iso.sha256
```


### iso-download.sh

接著執行下面的指令，就會下載剛剛「iso-download.txt」裡面所列的檔案

``` sh
wget -c -i iso-download.txt
```

> 關於「`-c`」指的是續傳

> 關於「`-i iso-download.txt`」，指的是下載「`iso-download.txt`」裡面所列的檔案




## Boot ISO

> 簡單「[驗證](#驗證)」過「下載完成的ISO檔案」，接下來可以選擇不同的「[Boot ISO](https://samwhelp.github.io/note-about-mxlinux/read/core/iso/boot-iso.html)」方式。





## 驗證


### sha256sum

* [man sha256sum](https://manpages.debian.org/bookworm/coreutils/sha256sum.1.en.html)

執行

``` sh
wget -c https://sourceforge.net/projects/mx-linux/files/Final/Xfce/MX-25_Xfce_x64.iso.sha256

sha256sum -c MX-25_Xfce_x64.iso.sha256
```

會看到類似如下的內容

```
MX-25_Xfce_x64.iso: OK
```

執行

``` sh
wget -c https://sourceforge.net/projects/mx-linux/files/Final/KDE/MX-25_KDE_x64.iso.sha256

sha256sum -c MX-25_KDE_x64.iso.sha256
```

會看到類似如下的內容

```
MX-25_KDE_x64.iso.sha256: OK
```

執行

``` sh
wget -c https://sourceforge.net/projects/mx-linux/files/Final/Fluxbox/MX-25_fluxbox_x64.iso.sha256

sha256sum -c MX-25_fluxbox_x64.iso.sha256
```

會看到類似如下的內容

```
MX-25_fluxbox_x64.iso: OK
```
