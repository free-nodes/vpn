## 2026最新VPS搭建Shadowsocks翻墙梯子教程含一键脚本

最新VPS搭建Shadowsocks翻墙梯子教程，只需要简单的三个步骤就可以自己动手搭建Shadowsocks，详细图文教程，Shadowsocks一键脚本安装，整个安装过程十分简单容易上手。

![最新VPS搭建Shadowsocks教程](./assets/1684751014-shadowsocks-1024x683.jpg)最新Shadowsocks搭建教程

## Shadowsocks搭建详细图文教程

打开浏览器访问Google成功返回Google首页结果，就说明搭建Shadowsocks成功了，如何搭建呢？只需要简单的三个步骤就可以自己搭建Shadowsocks，下面就详细介绍Shadowsocks搭建步骤。

**Total Time:** 30 minutes

### 前期准备

![Bandwagonhost](./assets/1684814167-Bandwagonhost-com.jpg)

需要一台适合搭建Shadowsocks翻墙梯子的VPS服务器，VPS服务器操作系统推荐使用Linux操作系统，如Debian、CentOS、Ubuntu都可以。

### 第一步：创建Shadowsocks服务器

![创建服务器](./assets/1687659427-vps.jpg)

如果已经拥有VPS服务器的朋友可以跳过这一部分，没有服务器的朋友可以先创建Shadowsocks服务器，推荐使用搬瓦工VPS服务器，网络线路速度和稳定性一直以来都比较不错，同时搬瓦工还运营着自己的翻墙机场。
选择VPS服务器要从以下五个方面综合考虑去选择，分别是：
1、选择海外VPS服务商；
2、选择大牌VPS服务商；
3、是否支持更换IP地址；
4、是否可更换机房；
5、主机配置。
特别需要注意的是，在购买完成之后，需要验证服务器IP是否被封，可使用IP可用性工具来对购买的服务器进行测试，这一步至关重要。

### 第二步：连接Shadowsocks服务器

![连接服务器](./assets/1687659420-xshell.jpg)

经过第一步创建好了服务器之后，现在就需要来连接Shadowsocks服务器，电脑端推荐使用Xshell来链接Shadowsocks服务器，可点击[Xshell官网](https://www.xshell.com/zh/free-for-home-school/)下载最新版，安装过程和普通的软件安装一样，很简单就不展开描述，在Xshell安装完成之后，就可以使用Xshell来连接Shadowsocks服务器，具体步骤如下：
1、打开XShell；
2、点击菜单栏【文件】，位于软件左上角；
3、点击【新建】；
4、名称随意，协议选择SSH，主机你的服务器IP（外网IP），端口默认22不变（映射端口和自设端口除外）；
5、点击确定；
6、在左侧会话管理器，选中刚添加的会话配置双击打开，可能会出现SSH安全警告，点击接受并保存即可；
7、提示输入用户名账号和密码，一般没特别设定用户名就是root，输入后记得点保存(没有提示可能IP被墙)；
8、进入服务器后，就可以运行一键安装Shadowsocks脚本代码了。

### 第三步：Shadowsocks搭建

![一键搭建](./assets/1687659424-onclick.jpg)

在第二步成功连接Shadowsocks服务器之后，就可以使用Shadowsocks一键安装脚本进行Shadowsocks搭建了，整个过程都是完全自动的，只需要按照提示选择几个参数即可。

**Supply:**

- BandwagonHost
- Vultr
- Linode

**Tools:**

- Xshell
- JuiceSSH

### Shadowsocks一键脚本搭建教程

本文以CentOS为例进行演示。

#### 安装Wget

成功连接服务器后，首先运行以下命令安装 Wget 组件，Wget是一个在网络上进行下载的简单而强大的自由软件。

```
yum install -y wget
```

#### 执行Shadowsocks一键安装脚本

此一键搭建Shadowsocks/SS服务器脚本由 秋水逸冰(Teddysun) 制作，而且一直在更新，目前支持 CentOS 6+、Debian 7+、Ubuntu 12+ 及以上系统版本，内存要求：≥128M，不支持“WS+TLS+CDN”，也不需要绑定域名。

```
wget --no-check-certificate -O shadowsocks-all.sh https://raw.githubusercontent.com/teddysun/shadowsocks_install/master/shadowsocks-all.sh
chmod +x shadowsocks-all.sh
./shadowsocks-all.sh 2>&1 | tee shadowsocks-all.log
```

将以上命令粘贴到 Xshell 窗口，回车执行代码，然后会提示有以下4种安装选项，如下图所示。

![Shadowsocks 一键安装脚本](./assets/1709474757-shadowsocks-install-01.jpg)Shadowsocks 一键安装脚本

这里选第1个，搭建Shadowsocks/SS服务器。如下图所示。

![Shadowsocks 一键安装脚本 Shadowsocks-Python](./assets/1709474961-shadowsocks-install-02.jpg)Shadowsocks-Python

输入数字“1”后回车，然后进入Shadowsocks服务器的参数配置选项，首先是服务器连接密码。如下图所示。

![Shadowsocks 一键安装脚本配置 Shadowsocks 服务器密码](./assets/1709475060-shadowsocks-install-03.jpg)配置 Shadowsocks 服务器密码

接着选择 Shadowsocks 服务器端口，如没有特别需求一般选择默认即可。如下图所示。

![Shadowsocks 一键安装脚本配置 Shadowsocks 服务器端口](./assets/1709475142-shadowsocks-install-04.jpg)配置 Shadowsocks 服务器端口

接着选择加密方式即算法，建议选择 `chacha20` 相关的加密方式（因为这些新加密方式的抗封锁效果更好）。如下图所示。

![Shadowsocks 一键安装脚本配置 Shadowsocks 服务器加密方式](./assets/1709475460-shadowsocks-install-05.jpg)配置 Shadowsocks 服务器加密方式

当以上参数选项都输入完毕后，敲击回车键。然后系统会提示“`Press any key to start…or Press Ctrl+C to cancel`“，即按任意键继续。如下图所示。

![Shadowsocks 一键安装脚本开始安装](./assets/1709475512-shadowsocks-install-06.jpg)Shadowsocks 一键安装脚本开始安装

当我们按任意键之后，系统会进入安装Shadowsocks服务的过程，稍等片刻即可完成。安装Shadowsocks服务成功完成后，如下图所示。

![Shadowsocks 一键安装脚本安装完成](./assets/1709475549-shadowsocks-install-07.jpg)Shadowsocks 一键安装脚本安装完成

如上图所示，其中各项参数释义如下：

- Your Server IP :你的服务器 IP 地址；
- Your Server Port :你的服务器端口；
- Your Password :你的连接密码；
- Your Encryption Method:你的加密方式；
- Your QR Code:你的SS链接；
- Your QR Code has been saved as a PNG file path:你的SS链接二维码图片的存放位置。

至此，你已经成功搭建Shadowsocks/SS服务器，现在就可以使用了。

## Shadowsocks客户端连接Shadowsocks

本文以Windows平台下的Shadowsocks客户端v2rayN举例来连接Shadowsocks服务器，其它平台客户端的连接方式基本都大同小异。

首先[下载v2RayN](https://free-nodes.github.io/v2rayn/v2rayn_download.html)，下载完成之后解压即可使用，解压后的目录如下图所示，不同版本的文件数量可能会有不同，这个不必纠结，只要能正常链接Shadowsocks服务器即可。

[![v2rayN 安装文件目录](./assets/1709514705-v2rayN-Floder.jpg)](https://www.tizidajian.com/wp-content/uploads/2023/05/1709514705-v2rayN-Floder.jpg)v2rayN 安装文件目录

单击鼠标右键以管理员身份运行 `v2rayN.exe` 即可开始使用，程序启动后会最小化到任务右小角的托盘，鼠标双击蓝色的 `V` 字小图标，即可打开软件的主界面。

### 从剪贴板导入方式添加Shadowsocks服务器

首先复制Shadowsocks服务器的节点地址，即以 `ss://` 开头的链接。

然后点击软件主界面的`服务器`，选择**从剪贴板导入批量URL**即可导入节点信息，如下图所示。

[![v2rayN 从剪贴板导入批量URL](./assets/1709515139-v2rayN-add-Server-from-Clipboard.jpg)](https://www.tizidajian.com/wp-content/uploads/2023/05/1709515139-v2rayN-add-Server-from-Clipboard.jpg)v2rayN 从剪贴板导入批量URL

### 手动添加Shadowsocks服务器

点击软件主界面的`服务器`，选择 `添加[Shadowsocks]服务器`，如下图所示。

[![v2rayN 添加 Shadowsocks 服务器节点](./assets/1709546644-v2rayN-add-Server-Shadowsocks-Server.jpg)](https://www.tizidajian.com/wp-content/uploads/2023/05/1709546644-v2rayN-add-Server-Shadowsocks-Server.jpg)v2rayN 添加 Shadowsocks 服务器节点

在添加窗口输入Shadowsocks服务器节点信息，即可配置Shadowsocks服务器信息，然后点击确定保存，如下图所示。

[![v2rayN 配置 Shadowsocks 服务器节点信息](./assets/1709546675-v2rayN-add-Server-Shadowsocks-Server-Config.jpg)](https://www.tizidajian.com/wp-content/uploads/2023/05/1709546675-v2rayN-add-Server-Shadowsocks-Server-Config.jpg)v2rayN 配置 Shadowsocks 服务器节点信息

至此使用Shadowsocks客户端连接Shadowsocks就完成了，更详细教程可参考[v2rayN使用教程快速入门篇](https://github.com/clashbk/clash/wiki/v2rayn)。