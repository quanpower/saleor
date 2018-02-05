[![Saleor](http://getsaleor.com/mr-saleor-readme.png)](http://getsaleor.com)


Saleor
======

Avast ye landlubbers! Saleor is an open-source e-commerce storefront for Python and Django.

[Saleor homepage](http://getsaleor.com/)

[![Build Status](https://travis-ci.org/mirumee/saleor.png?branch=master)](https://travis-ci.org/mirumee/saleor)
[![Requirements Status](https://requires.io/github/mirumee/saleor/requirements.svg?branch=master)](https://requires.io/github/mirumee/saleor/requirements/?branch=master)
[![codecov.io](http://codecov.io/github/mirumee/saleor/coverage.svg?branch=master)](http://codecov.io/github/mirumee/saleor?branch=master)

* * *

Your feedback
-------------

Do you use Saleor as an e-commerce platform?
Fill out this short survey and help us grow. It will take just a minute, but mean a lot!

[Survey](https://mirumee.typeform.com/to/sOIJbJ)

* * *

Usage
-----

See the [Saleor docs](https://saleor.readthedocs.io) for installation and deployment instructions.


Demo
----

Want to see Saleor in action?

[Saleor live demo](http://demo.getsaleor.com/)

[Saleor Dashboard (admin area) demo](http://demo.getsaleor.com/dashboard/)

Or launch the demo on a free Heroku instance.

[![Deploy](https://www.herokucdn.com/deploy/button.png)](https://heroku.com/deploy)

Login credentials: `admin@example.com`/`admin`


Commercial support
------------------

Disclaimer: everything you see here is open and free to use as long as you comply with the [license](LICENSE). It is not a bait to force you to pay us later and we promise to do our best to fix bugs and improve the code.

Some situations however call for extra code being written. Whether you need us to cover an exotic use case or build you a custom e-commerce appliance, our team can help.

### Mirumee Software

http://mirumee.com

hello@mirumee.com


### postgreSQL

-------
su postgres

psql

\password postgres

CREATE USER saleor WITH PASSWORD 'saleor';

postgres=> grant saleor to postgres;

postgres=> CREATE DATABASE saleor OWNER saleor;

\q

-------

sudo -u postgres createuser --superuser dbuser
sudo -u postgres psql
\password dbuser
\q
sudo -u postgres createdb -O dbuser exampledb

-------


ALTER USER postgres WITH SUPERUSER;

(1)列出所有的数据库
mysql: show databases
psql: \l或\list
(2)切换数据库
mysql: use dbname
psql: \c dbname

(3)列出当前数据库下的数据表
mysql: show tables
psql: \d

(4)列出指定表的所有字段
mysql: show columns from table name
psql: \d tablename

(5)查看指定表的基本情况
mysql: describe tablename
psql: \d+ tablename

(6)退出登录
mysql: quit 或者\q
psql:\q


\h      #查看所有的sql关键字
\?      #命令行操作的帮助
\d      #查看当前schema 中所有的表
\q      #退出pg命令行
\d      #schema.table 查看表的结构
\x      #横纵显示切换
\dT+    #显示扩展类型相关属性及描述
\dx     #显示已安装的扩展插件
\l      #列出所有的数据库
\timing #显示执行时间
\c database_name        #切换数据库
set search to schema    #切换schema
explain sql             #解释或分析sql执行过程

psql -U user_name -d database_name -h serverhost

删除相关的安装
sudo apt-get --purge remove postgresql\*

删除配置及文相关件
sudo rm -r /etc/postgresql/
sudo rm -r /etc/postgresql-common/
sudo rm -r /var/lib/postgresql/

删除用户和所在组
sudo userdel -r postgres
sudo groupdel postgres

重新安装
sudo apt-get install postgresql


pg_dump -U smartlinkcloud smartlinkcloud | gzip > ~/smartlinkcloud.gz

恢复：
   gunzip -c /vendemo.gz | psql -U postgres bk02
