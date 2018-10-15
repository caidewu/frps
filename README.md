# frp内网穿透服务端自动运行脚本

> 该项目fork https://github.com/clangcn/onekey-install-shell，由于onekey-install-shell这个项目名字语意不明，所以这里新建了一个项目

> 项目基于[fatedier/frp](https://github.com/fatedier/frp)


## 如何使用

> 该项目是运行在外网服务器上，以下的所有操作确保是在外网服务器中进行

- 下载脚本

```
wget --no-check-certificate https://raw.githubusercontent.com/caidewu/frps/master/install.sh -O ./install.sh
```

- 安装

```
# 安装过程会有一系列去要确人的配置信息，没有特殊要求用default的就好了
./install.sh install
```

安装成功会生成类似如下的配置信息， 并且启动服务

```
============== Check your input ==============
You Server IP      : 100.100.100.100
Bind port          : 7000
kcp support        : true
vhost http port    : 10080
vhost https port   : 10443
Dashboard port     : 7500
Dashboard user     : admin
Dashboard password : xxxxxx
token              : xxxxxxxx
tcp_mux            : true
Max Pool count     : 50
Log level          : info
Log max days       : 3
Log file           : enable
==============================================
```

- 测试服务（以上面配置信息为例）

用浏览器可以直接访问：`http://100.100.100.100:7500`, (确保外网服务器安全组的7000，7500端口是打开的)

![frps管理后台](/example1.png)

- 其他常用命令

```
frps {start|stop|restart|status|config|version}
```

## 安装客户端程序

客户端安装运行步骤[在此](https://github.com/caidewu/frpc)

## 相关项目

- [客户端自动运行脚本](https://github.com/caidewu/frpc)