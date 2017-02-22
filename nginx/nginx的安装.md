# nginx Liunx 系统下的安装
## 1. 软件包下载 ：[nginx下载地址](http://nginx.org/)
##  2. 下载包解压：
```
tar -zxvf nginx-1.10.3.tar.gz
```
## 3. 安装nginx前需要先安装依赖包
> nginx是C语言开发，建议在linux上运行，本教程使用Centos6.5作为安装环境。
-	gcc
>安装nginx需要先将官网下载的源码进行编译，编译依赖gcc环境，如果没有gcc环境，需要安装gcc：
```
yum install gcc-c++ 
```
- PCRE
> PCRE(Perl Compatible Regular Expressions)是一个Perl库，包括 perl 兼容的正则表达式库。nginx的http模块使用pcre来解析正则表达式，所以需要在linux上安装pcre库。
```
yum install -y pcre pcre-devel
```
*注：pcre-devel是使用pcre开发的一个二次开发库。nginx也需要此库。*
- zlib
> zlib库提供了很多种压缩和解压缩的方式，nginx使用zlib对http包的内容进行gzip，所以需要在linux上安装zlib库。
```
yum install -y zlib zlib-devel
```

- openssl
> OpenSSL 是一个强大的安全套接字层密码库，囊括主要的密码算法、常用的密钥和证书封装管理功能及SSL协议，并提供丰富的应用程序供测试或其它目的使用。nginx不仅支持http协议，还支持https（即在ssl协议上传输http），所以需要在linux安装openssl库。
```
yum install -y openssl openssl-devel
```
## 4. nginx 安装步骤
