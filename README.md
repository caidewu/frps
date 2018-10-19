# frp内网穿透服务端自动运行脚本

> 项目基于[fatedier/frp](https://github.com/fatedier/frp)


## 如何使用

> 该项目是运行在外网服务器上，以下的所有操作确保是在外网服务器中进行

### 在云服务器或具有独立IP的外网服务器上clone本项目

```
git clone https://github.com/caidewu/frpc.git
```

### 配置

> 根据自己情况去修改以下几个配置项

```
[common]
# frp通信端口
bind_port = 7000

# 和bind_port保持一致就好
kcp_bind_port = 7000

# frps控制台端口
dashboard_port = 7500

# 控制台登陆名和密码
dashboard_user = admin
dashboard_pwd = 123456

# 与客户端通信的token，随便一个字符串，和frpc中配置的一样就行
privilege_token = xxxxxxxxxxx
```

### 启动frps

```
./startup.sh
```

### 测试服务（以上面配置信息为例）

用浏览器可以直接访问：`http://100.100.100.100:7500`, (确保外网服务器安全组的7000，7500端口是打开的)

![frps管理后台](/example1.png)



## 安装客户端程序

客户端安装运行步骤[在此](https://github.com/caidewu/frpc)

## 相关项目

- [客户端自动运行脚本](https://github.com/caidewu/frpc)
