# mysql-安装
系统 centos 7.6

1: 安装包  wget http://dev.mysql.com/get/mysql-community-release-el7-5.noarch.rpm

2: 然后解压文件  rpm -ivh mysql-community-release-el7-5.noarch.rpm

3: 安装mysql server 服务 yum install mysql-community-server

4: 因为是 centos 7.6 系统，所以需要 重启服务  service mysqld restart

5: 第一次进入没有密码 直接 mysql -uroot 即可

6: 修改mysql 字符集 统一使用utf-8 vi /etc/my.cnf 然后在最后一行加上 default-character-set =utf8

7：修改密码 set password for 'root'@'localhost'=password('123456'); 

8: mysql -uroot -p -hlocalhost 然后输入密码检测是否设置成功

9: grant all privileges on *.* to root@'%'identified by '123456'; 设置远程登录，去防火墙放开端口即可， 一般是3306
