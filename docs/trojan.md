## 2026最新VPS搭建Trojan翻墙梯子教程含一键脚本

最新VPS搭建Trojan翻墙梯子教程，只需要简单的三个步骤就可以自己动手搭建Trojan，详细图文教程，Trojan一键脚本安装，整个安装过程十分简单容易上手。

![最新VPS搭建Trojan教程](./assets/1684750986-trojan-1024x683.jpg)最新Trojan搭建教程



## 什么是Trojan？

Trojan是一种利用TLS加密方式的协议，Trojan通过将通信流量伪装成常见的HTTPS流量，来防止流量被检测和干扰，以此来达到翻墙的目的。

## Trojan搭建详细图文教程

打开浏览器访问Google成功返回Google首页结果，就说明搭建Trojan成功了，如何搭建呢？只需要简单的三个步骤就可以自己搭建Trojan，下面就详细介绍Trojan搭建步骤。

**Total Time:** 30 minutes

### 前期准备

![Bandwagonhost](./assets/1684814167-Bandwagonhost-com-1778765643037-2.jpg)

1、一台适合搭建Trojan翻墙梯子的**VPS服务器**，VPS服务器操作系统推荐使用Linux操作系统，如Debian、CentOS、Ubuntu都可以。
2、一个用来伪装流量的**域名**，推荐使用NameSilo或者免费域名（可自行搜索），并对域名进行解析，解析绑定至准备的VPS服务器，具体域名解析步骤可自行搜索相关教程。
3、一些连接Trojan服务器常用的服务器连接软件，如Xshell、JuiceSSH、Cmder等。

### 第一步：创建Trojan服务器

![创建服务器](./assets/1687659427-vps-1778765643037-4.jpg)

如果已经拥有VPS服务器的朋友可以跳过这一部分，没有服务器的朋友可以先创建Trojan服务器，推荐使用搬瓦工VPS服务器，网络线路速度和稳定性一直以来都比较不错。
选择VPS服务器要从以下五个方面综合考虑去选择，分别是：
1、选择海外VPS服务商；
2、选择大牌VPS服务商；
3、是否支持更换IP地址；
4、是否可更换机房；
5、主机配置。
特别需要注意的是，在购买完成之后，需要验证服务器IP是否被封，可使用IP可用性工具来对购买的服务器进行测试，这一步至关重要。

### 第二步：连接Trojan服务器

![连接服务器](./assets/1687659420-xshell-1778765643037-6.jpg)

经过第一步创建好了服务器之后，现在就需要来连接Trojan服务器，电脑端推荐使用Xshell来链接Trojan服务器，可点击[Xshell官网](https://www.xshell.com/zh/free-for-home-school/)下载最新版，安装过程和普通的软件安装一样，很简单就不展开描述，在Xshell安装完成之后，就可以使用Xshell来连接Trojan服务器，具体步骤如下：
1、打开XShell；
2、点击菜单栏【文件】，位于软件左上角；
3、点击【新建】；
4、名称随意，协议选择SSH，主机你的服务器IP（外网IP），端口默认22不变（映射端口和自设端口除外）；
5、点击确定；
6、在左侧会话管理器，选中刚添加的会话配置双击打开，可能会出现SSH安全警告，点击接受并保存即可；
7、提示输入用户名账号和密码，一般没特别设定用户名就是root，输入后记得点保存(没有提示可能IP被墙)；
8、进入服务器后，就可以运行一键安装Trojan脚本代码了。

### 第三步：Trojan搭建

![一键搭建](./assets/1687659424-onclick-1778765643037-8.jpg)

在第二步成功连接Trojan服务器之后，就可以使用Trojan一键安装脚本进行Trojan搭建了，整个过程都是完全自动的，只需要按照提示选择几个参数即可。

**Supply:**

- BandwagonHost
- Vultr
- Linode

**Tools:**

- Xshell
- JuiceSSH

### Trojan一键脚本搭建教程

本文以CentOS为例进行演示。

#### 安装Wget

成功连接服务器后，首先运行以下命令安装 Wget 组件，Wget是一个在网络上进行下载的简单而强大的自由软件。

```
yum install -y wget
```

#### 执行Trojan一键安装脚本

这个一键Trojan脚本，能自动获取Trojan官方最新版本进行部署，全智能化安装，在Xshell命令界面输入以下命令回车执行即可。

```
wget -N --no-check-certificate -q -O trojan_install.sh "https://raw.githubusercontent.com/V2RaySSR/Trojan/master/trojan_install.sh" && chmod +x trojan_install.sh && bash trojan_install.sh
```

输入 1 后回车，图下图所示。

输入之前已经解析好的域名，一般解析完域名后需要等待大概十分钟左右才能解析成功，比如我解析的是 `wall.tizidajian.com`，输入域名后直接按回车键执行。

显示以下信息就代表安装成功了。



