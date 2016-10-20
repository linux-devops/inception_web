# mysqlcheck：采用django开发

# 数据库地址：
host:127.0.0.1
port:3306
user:mysqlcheck_dev
pwd:mysqlcheck_dev




# 环境说明
Django==1.8.7    
> 注意: 只有Django8支持, 高版本暂不支持, eg: patterns这个只有该版本能用

djangorestframework==3.1.3
django-rest-swagger==0.3.4
MySQL-python==1.2.5


也可使用requirements一体化安装：
requirements.txt 
安装方法:  pip install -r requirements

运行方法：python manage.py runserver 8080 
打开浏览器，输入：http://localhost:8080/ 
manage.py路径：mysqlcheck\manage.py


# django 项目说明
1.mysqlcheck\mysqlcheck\settings.py  
该文件包含了所有有关这个Django项目的配置信息，均大写
比如：
a.数据库配置
b.模板配置
c.默认url指定
d.应用程序绑定
参考资料：http://zhidao.baidu.com/link?url=i5W1Xi0Lu_tOxbK4mwnu_qrUfC8WXMX7D-xrZGgm45AQwjU9ifHQ4y4JSO7JrtEHi8OmO0QI5JWrtxp61WLF3K

2.mysqlcheck\mysqlcheck\urls.py
默认url指定，路由规则。
该项目路由为动态加载，加载指定应用程序下的url.py(mysqlcheck\webapp\urls.py 下读取数据库表：superdba_menu)  


3.models.py层
一般位于应用程序目录下，该项目地址：mysqlcheck\webapp\models.py


4.views.py层（.net、java、PHP中叫控制器control）
一般位于应用程序目录下，该项目地址：mysqlcheck\webapp\views.py
该项目控制层进行了扩展，路径(mysqlcheck\webapp\view\*)

5.模板及静态资源文件（templates、static） ，也就是视图层
所有html的前端效果在这里定义，路径项目根目录下：mysqlcheck\templates、mysqlcheck\static


总结：
MVC在django中变成了MTV
M：数据库交互层
V：控制层
T：前端视图层



# 工具调试篇：
前提先装好python 及其运行环境

a)eclipse
百度搜：eclipse 调试python
参考资料：
http://iluoxuan.iteye.com/blog/1625940
http://my.oschina.net/xshuai/blog/381833
http://www.cnblogs.com/linjiqin/p/3579995.html

b)visual studio
主要是要安装PTVS插件(https://github.com/Microsoft/PTVS/releases/v2.2)
参考资料：
http://www.cnblogs.com/JamesLi2015/archive/2012/01/05/2312678.html
http://www.oschina.net/p/PTVS/


c)如果你不需要调试，或安装调试失败
直接用文本编辑工具编，然后运行看报错提示
（txt、Notepad++、sublime等等）


 
