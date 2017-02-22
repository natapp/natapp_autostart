Natapp For 树莓派 开机启动脚本

##运行natapp客户端
1. 在 https://natapp.cn 官网 下载客户端.
放在目录 `/usr/natapp/`
运行
```
chmod a+x /usr/natapp/natapp
```
给予可执行权限
 
2.下载`config.ini`放置在同级目录,config 配置说明请见 https://natapp.cn/article/config_ini

将authtoken等配置 写入 config.ini中.

需要注意的是 务必关闭 关闭Web管理界面 (登录网站->我的隧道->配置)

3.测试运行情况
```
./usr/natapp/natapp
```
实际测试穿透应用,确保无误,后关闭客户端

##自启动脚本
4.将启动脚本 ([下载](https://raw.githubusercontent.com/natapp/natapp_autostart/master/RaspberryPi/natapp)) 放在 `/etc/init.d/` 下

给予 755权限
```
chmod 755 /etc/init.d/natapp
```

5.测试 init.d 启动
运行
```
/etc/init.d/natapp start
```
同3,确保穿透应用运行无误.

6.加入开机自启动
```
/etc/init.d/natapp enable && echo on
```

7.
```
reboot
```
正常的话,已经可以自动了

####相关命令
```
/etc/init.d/natapp start    #开启
/etc/init.d/natapp stop     #关闭
/etc/init.d/natapp restart  #重启

/etc/init.d/natapp enable && echo on    #加入开机启动
/etc/init.d/natapp disable && echo off  #取消开机启动
```

