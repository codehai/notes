# notes
------

## Nginx

* 从容停止Nginx：kill -QUIT 主进程号
* 快速停止Nginx：kill -TERM 主进程号
* 强制停止Nginx：pkill -9 nginx

## Linux相关命令

### 用户切换
* user→root用户切换:sudo su
* root→user用户切换:su user

### 文件查找
* 根据文件内容
grep -nr 'foo' * 

## apache2

### apache文件路径
* 如果apt-get命令安装:
apache配置文件:/etc/apache2/sites-available
apache模块路径：/usr/sbin/apachectl
web目录:/var/www/
* 如果采用源代码安装
一般默认安装在/usr/local/apache2目录下

### apache相关命令
* 启动apache服务:
sudo /etc/init.d/apache2 start
* 重启apache服务:
sudo /etc/init.d/apache2 restart
* 停止apache服务:
sudo /etc/init.d/apache2 stop

## CSS

* CSS footer 置于页面底部
https://codepen.io/cbracco/pen/zekgx

* 图片居中
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <title>Document</title>
    <style>
        .pics-container {
            height: 100px;
            width: 100px;
            overflow: hidden;
            text-align: center;
            margin: 0 auto;
        }
        .pics-container img {
            height: 100px;
            max-width: none;
            margin: 0 -100%;
        }
    </style>
</head>
<body>
    <div class="pics-container">
        <!-- 这里有个问题，如果图片是等高宽的话，会等比缩小，看不出hidden的效果 -->
        <img src="1.jpg">
    </div>
</body>
</html>
```

## 杂项

### 编码转换

* 前面不带u的unicode编码转中文python方法：
```python
nick =  data['author_dat']['nick']
json.loads("\"" + nick+ "\"")
print '<p><a class="p" target="_blank" href="http://www.duitang.com/people/1629580/">'+json.loads("\"" + nick+ "\"")+'</a></p></li></ul></div></div>'
```
* js方法:
```javascript
function uToc(u){
	var nick = JSON.parse("\"" + u+ "\"");
	return nick;
}
```

