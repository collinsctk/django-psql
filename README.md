# django-psql
# 亁颐堂Django实验用PSQL数据库

### 执行如下脚本拉起容器
```shell
cd /
git clone https://github.com/collinsctk/django-psql.git
cd django-psql/
docker-compose up -d
```

### 查看容器运行状态
```shell
[root@PSQL django-psql]# docker ps
CONTAINER ID   IMAGE            COMMAND                   CREATED          STATUS          PORTS                                       NAMES
a224720bc24c   postgres:12.15   "docker-entrypoint.s…"   20 seconds ago   Up 19 seconds   0.0.0.0:5432->5432/tcp, :::5432->5432/tcp   django-psql_qyt-psql_1
```

### 如果要重置之前的migration, 请按照如下步骤操作
```shell
# 删除所有"migrations"目录下, 除了__init__.py以外的其他文件与目录
[root@Django qytdb]# cd migrations/
[root@Django migrations]# ls
0001_initial.py  __init__.py  __pycache__
[root@Django migrations]# rm -f 0001_initial.py 
[root@Django migrations]# rm -rf __pycache__/
```
