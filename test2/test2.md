## 实验2：用户及权限管理
### 1.实验目的
掌握用户管理、角色管理、权根维护与分配的能力，掌握用户之间共享对象的操作技能。
### 2.实验内容
Oracle有一个开发者角色resource，可以创建表、过程、触发器等对象，但是不能创建视图。本训练要求：

- 在pdborcl插接式数据中创建一个新的本地角色longkefan，该角色包含connect和resource角色，同时也包含CREATE VIEW权限，这样任何拥有longkefan的用户就同时拥有这三种权限。
- 创建角色之后，再创建用户user_longkefan，给用户分配表空间，设置限额为50M，授予longkefan角色。
- 最后测试：用新用户user_longkefan连接数据库、创建表，插入数据，创建视图，查询表和视图的数据。

### 3.实验步骤
- 第1步：以system登录到pdborcl，创建角色longkefan和用户user_longkefan，并授权和分配空间：
```sql
$ sqlplus system/123@pdborcl
SQL> CREATE ROLE longkefan_view;
Role created.
SQL> GRANT connect,resource,CREATE VIEW TO longkefan_view;
Grant succeeded.
SQL> CREATE USER longkefan1 IDENTIFIED BY 123 DEFAULT TABLESPACE users TEMPORARY TABLESPACE temp;
User created.
SQL> ALTER USER longkefan_ QUOTA 50M ON users;
User altered.
SQL> GRANT longkefan_view TO longkefan_;
Grant succeeded.
SQL> exit
```
    运行结果如下：
![avatar](1_1.png)
![avatar](2.png)
![avatar](3.png)
- 第2步：新用户longkefan_连接到pdborcl，创建表mytable和视图myview，插入数据，最后将myview的SELECT对象权限授予hr用户。
```sql
$ sqlplus longkefan_/123@pdborcl
SQL> show user;
USER is "longkefan_"
SQL> CREATE TABLE mytable (id number,name varchar(50));
Table created.
SQL> INSERT INTO mytable(id,name)VALUES(1,'zhang');
1 row created.
SQL> INSERT INTO mytable(id,name)VALUES (2,'wang');
1 row created.
SQL> CREATE VIEW myview AS SELECT name FROM mytable;
View created.
SQL> SELECT * FROM myview;
NAME
--------------------------------------------------
zhang
wang
SQL> GRANT SELECT ON myview TO hr;
Grant succeeded.
SQL>exit
```
    运行结果如下：
![avatar](2_1.png)

- 第3步：用户hr连接到pdborcl，查询user_longkefan授予它的视图myview
```sql
$ sqlplus hr/123@pdborcl
SQL> SELECT * FROM longkefan_.myview;
NAME
--------------------------------------------------
zhang
wang
SQL> exit
```
    运行结果如下：
![avatar](3_1.png)
### 查看数据库的使用情况
以下样例查看表空间的数据库文件，以及每个文件的磁盘占用情况。
```sql
$ sqlplus system/123@pdborcl

SQL>SELECT tablespace_name,FILE_NAME,BYTES/1024/1024 MB,MAXBYTES/1024/1024 MAX_MB,autoextensible FROM dba_data_files  WHERE  tablespace_name='USERS';

SQL>SELECT a.tablespace_name "表空间名",Total/1024/1024 "大小MB",
 free/1024/1024 "剩余MB",( total - free )/1024/1024 "使用MB",
 Round(( total - free )/ total,4)* 100 "使用率%"
 from (SELECT tablespace_name,Sum(bytes)free
        FROM   dba_free_space group  BY tablespace_name)a,
       (SELECT tablespace_name,Sum(bytes)total FROM dba_data_files
        group  BY tablespace_name)b
 where  a.tablespace_name = b.tablespace_name;
 ```
     运行结果如下：
![avatar](3_2.png)