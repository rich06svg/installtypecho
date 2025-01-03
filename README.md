# 30分钟搭建 Typecho 个人博客教程
​
Typecho是一款PHP博客程序，相比于WordPress，Typecho显得更加的轻量级和简洁。现在越来越多的人倾向于用Typecho来搭建个人博客——众所周知，能跑WordPress的机器都不便宜。

Typecho是一款国人团结打造的开源博客系统，和WordPress一样是PHP语言开发的。主打开源、轻量。
​![typecho](https://i-blog.csdnimg.cn/direct/1853a162e4954d6990eb1fa4c4ceb619.png)
Typecho官网：[typecho.org](typecho.org)

博客演示（Joe）：[chenyifa.town](chenyifa.town)

## 1、域名注册
如果你已经有域名了当然可以不用管这一步。

国内的就是百度、阿里、腾讯，不过都需要实名认证，而且过程比较繁琐。

所以这里推荐海外大厂[dynadot](http://www.dynadot.com?s8H7b7S7i72dy8S)（走这个链接赠送5$），支持支付宝付款。

## 2、购买VPS
VPS可以用阿里云、腾讯云，海外可以是[HostVDS](https://hostvds.com/?affiliate_uuid=fbff2c4f-05e9-42e0-9e16-c071e6b8e55b)，主打性价比。
95折优惠码：HVDSFT5

## 3、域名解析
这里建议解析到Cloudflare，教程网上太多了。

## 4、安装宝塔面板
宝塔面板是国内开发的一个Linux可视化控制面板。

不过国内版有广告，而且必须登录账号，所以这个安装aaPanel（宝塔国际版）

更新组件
```bash
apt update -y && apt install -y curl && apt install -y socat && apt install wget -y
```
BBR加速
```bash
wget -N --no-check-certificate "https://raw.githubusercontent.com/chiakge/Linux-NetSpeed/master/tcp.sh" && chmod +x tcp.sh && ./tcp.sh
```
宝塔安装

Debian
```bash
wget -O install.sh http://www.aapanel.com/script/install-ubuntu_6.0_en.sh && bash install.sh aapanel
```
Ubuntu
```bash
wget -O install.sh http://www.aapanel.com/script/install-ubuntu_6.0_en.sh && sudo bash install.sh aapanel
```
Centos
```bash
yum install -y wget && wget -O install.sh http://www.aapanel.com/script/install_6.0_en.sh && bash install.sh aapanel
```
首次进入宝塔面板会让安装组件，个人比较倾向于用apache。

**注意：php需要选择7.4版本！**

## 5、安装Typecho

添加域名，完成后点击确认。
![aapanel](https://i-blog.csdnimg.cn/direct/974e1e95e85f44fa9323c0346aa6b417.png)
点击进入网站根目录。

将从typecho官网下载的源码上传到网站根目录，然后解压。
访问：
```bash
[你的域名]/install.php
```
之后填写设置的mysql数据库用户名、密码，以及网站信息就可以了。
访问：
```bash
[你的域名]/admin
```
进入网站管理后台。
