# mysql

# Windows修改MySQL用户root密码</br>
http://www.cnblogs.com/suke99/p/5311687.html
</br>
用UPDATE直接编辑user表</br>

用UPDATE直接编辑user表</br>
首先登录MySQL。</br>
\mysql\bin\>mysql -u root -p</br>
连接权限数据库： use mysql; 。</br>
改密码：update user set password=password("123") where user="root";（别忘了最后加分号） 。 </br>
刷新权限（必须步骤）：flush privileges;</br>
重新登录，输入新密码root就ok了；</br>
##修改phpmyadmin密码 
phpmyadmin里面配置文件config.inc.php里面的一个参数</br>
$cfg['Servers'][$i]['password']
</br></br></br></br>



# Mysql初始化root密码和允许远程访问
首先登录MySQL。</br>
</br>
\mysql\bin\>mysql -u root -p</br>
</br>
//赋予任何主机访问数据的权限</br>
mysql>GRANT ALL PRIVILEGES ON *.* TO 'root'@'%' WITH GRANT OPTION;</br>
//使修改生效</br>
mysql>FLUSH PRIVILEGES;</br>
//退出MySQL服务器</br>
mysql>EXIT;</br>

https://www.cnblogs.com/cnblogsfans/archive/2009/09/21/1570942.html
https://www.jianshu.com/p/26b52a1fb3dd
