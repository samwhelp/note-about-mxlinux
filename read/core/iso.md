---
title: ISO
nav_order: 1000
has_children: true
---


# ISO




## 主題

| 主題 |
| --- |
| [Download ISO](https://samwhelp.github.io/note-about-mxlinux/read/core/iso/download-iso.html) |
| [Boot ISO](https://samwhelp.github.io/note-about-mxlinux/read/core/iso/boot-iso.html) |




## Live Account

> Source Code: GitHub / MX-Linux / build-iso-mx / [build-iso](https://github.com/MX-Linux/build-iso-mx/blob/master/build-iso#L1183-L1191)

> 使用「MxLinux Live ISO」開機後，自動登入的帳號。

| Account  | Value  |
| -------- | ------ |
| Username | `demo` |
| Password | `demo` |


> 執行下面指令，更改目前登入帳號的密碼。

``` sh
sudo passwd $(whoami)
```


> 執行下面指令，移除目前登入帳號的密碼。

``` sh
sudo passwd -d $(whoami)
```
