# 采用docker-compose容器编排Zabbix组件

+ `docker-compose_v3_alpine_mysql_latest.yaml`
+ `server-mysql`
+ `web-nginx-mysql`
+ `.env_db_mysql`

## 使用

### 单主机

```
# 构建镜像
docker-compose build

# 启动容器
docker-compose up -d
```


### 服务器集群

```
# 构建镜像
docker-compose build

# push到私有镜像仓库
docker-compose push

# 发布服务
docker stack deploy -c docker-compose.yml zabbix
```

## References

+ [Zabbix docker官方代码库](https://github.com/zabbix/zabbix-docker)
