# patent-download
一个中国专利数据的免费下载系统

功能
====
- 免费获取大量专利数据
- 可指定检索表达式
- 数据写入数据库(自动建表)
- 定制日志
- 多线程下载


使用说明
====
- 作者:刘纪春
- 依赖:jdk8
- 使用配置:
配置文件在conf下(均为UTF-8英文标点):

* 配置hibernate.cfg.xml中有关于数据库连接的配置项,修改为自己所需要的
```
<property name="dialect">org.hibernate.dialect.MySQL5InnoDBDialect</property><!--mysql使用可以不修改-->
<property name="connection.password">root</property>
<property name="connection.username">root</property>
<property name="connection.url">jdbc:mysql://localhost:3306/patent</property>
<property name="connection.driver_class">com.mysql.jdbc.Driver</property>
```

* 配置log4j.properties文件配置项,修改为自己的路径
log4j.appender.R.File:日志文件输出地址

* 配置star.properties文件配置项,修改为自己的需求
```
queryFormula:查询表达式
userName:patentstar用户名
password:patentstar密码
threadNum:设置线程数,不建议大于20
timeout:设置连接超时时间,单位为毫秒
```

* 启动:在配置好java_home的情况下单击startUp.bat启动下载