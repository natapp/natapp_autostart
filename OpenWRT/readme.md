Natapp For OpenWRT 开机启动脚本

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
确保无误,关闭客户端


