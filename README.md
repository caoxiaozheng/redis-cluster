这个redis集群为3.2.12版本，在原有的集群基础上增加了redis密码。
集群启动命令
docker run  -d -p 7000:7000 -p 7001:7001 -p 7002:7002 -e SLAVES_PER_MASTER=0 --name redis-cluster2 redis-cluster:3.2.12
#SLAVES_PER_MASTER   是一个主节点对应几个从节点 默认一个节点
#redis_password   是集群的密码 默认 123456
#INITIAL_POR  为初始端口 默认从7000开始
#$MASTERS   集群主节点的数量 默认3个
