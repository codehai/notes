# notes

* Nginx

* 从容停止Nginx：
kill -QUIT 主进程号
快速停止Nginx：
kill -TERM 主进程号
强制停止Nginx：
pkill -9 nginx

* 用户切换
* user→root用户切换
sudo su
root→user用户切换
su user

* apache2

* 如果apt-get命令安装
apache配置文件:/etc/apache2/sites-available
apache模块路径：/usr/sbin/apachectl
web目录:/var/www/
如果采用源代码安装，一般默认安装在/usr/local/apache2目录下

Linux系统为Ubuntu
一、Start Apache 2 Server /启动apache服务
# /etc/init.d/apache2 start
or
$ sudo /etc/init.d/apache2 start
二、 Restart Apache 2 Server /重启apache服务
# /etc/init.d/apache2 restart
or
$ sudo /etc/init.d/apache2 restart
三、Stop Apache 2 Server /停止apache服务
# /etc/init.d/apache2 stop
$ sudo /etc/init.d/apache2 stop

* 编码转换

* 前面不带u的unicode编码转中文python方法：
nick =  data['author_dat']['nick']
json.loads("\"" + nick+ "\"")
print '<p><a class="p" target="_blank" href="http://www.duitang.com/people/1629580/">'+json.loads("\"" + nick+ "\"")+'</a></p></li></ul></div></div>'
js方法:
function uToc(u){
	var nick = JSON.parse("\"" + u+ "\"");
	return nick;
}

* CSS
* CSS foote 置于页面底部
https://codepen.io/cbracco/pen/zekgx
