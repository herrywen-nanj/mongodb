https://blog.csdn.net/zhiwule1314/article/details/103085386#mongodb_29
# mongodb
mongodb分布式分片副本集
# 分配端口
27018,27019   configsrv
27020,27021,27022   shardsvr
   clusterRole: shardsvr


40000    mongos
sharding:
   configDB: <string>

# 启动
## 分片以及配置设备
mongod -f mongodb.conf
## 路由设备
mongos -f mongodb.conf


# 相关配置
sh.addShard("shard-rs/worker2:27020,worker2:27021,worker2:27022")  



sh.enableSharding("test")  


sh.status()  


sh.shardCollection("test.herrywen",{"_id":1})  



sh.status()
