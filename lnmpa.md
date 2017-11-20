# lnmpa集成环境安装

## 安装流程

- wget -c http://soft.vpser.net/lnmp/lnmp1.4.tar.gz && tar zxf lnmp1.4.tar.gz && cd lnmp1.4 && ./install.sh lnmp
- 还可以在 ./install.sh 后面将lnmp替换lnmpa或lamp
- 地址失效可去lnmp官网
- 之后按照需求选择版本

## 安装缺失

- 环境安装完成后会缺失fileinfo拓展
- 这时可下载安装php版本的源码包，解压进入"cd /php-7.1.1/ext/fileinfo"
- 执行"/usr/local/php/bin/phpize"
- 执行"./configure --with-[php](http://cpro.baidu.com/cpro/ui/uijs.php?adclass=0&app_id=0&c=news&cf=1001&ch=0&di=128&fv=20&is_app=0&jk=e58366262e229521&k=php&k0=php&kdi0=0&luki=3&mcpm=0&n=10&p=baidu&q=mx163_cpr&rb=0&rs=1&seller_id=1&sid=2195222e266683e5&ssp2=1&stid=9&t=tpclicked3_hc&td=2004887&tu=u2004887&u=http%3A%2F%2Fwww%2Exker%2Ecom%2Fpage%2Fe2013%2F1130%2F130338%2Ehtml&urlid=0)-config=/usr/local/php/bin/php-config"
- 修改php.ini文件"vi /usr/local/php/etc/php.ini" 在该文件中加入"extension = fileinfo.so"
- 重起服务器

## lnmpa常用指令

- lnmp {start|stop|reload|restart|kill|status}
- lnmp {nginx|mysql|mariadb|pureftpd|httpd} {start|stop|reload|restart|kill|status}
- lnmp vhost {add|list|del}
- lnmp database {add|list|edit|del}
- lnmp ftp {add|list|edit|del|show}
- lnmp ssl add