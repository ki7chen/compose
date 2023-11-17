

#### 动态添加/删除节点

```bash
etcdctl --endpoints=${HOST_1}:2379,${HOST_2}:2379 member remove ${NAME_3}
etcdctl --endpoints=${HOST_1}:2379,${HOST_2}:2379 member add ${NAME_4} -peer-urls=http://${HOST_4}:2380
```


#### 查看集群状态

```bash
etcdctl -w table --endpoints=${HOST_1}:2379,${HOST_2}:2379,${HOST_3}:2379 endpoint status
etcdctl -w table --endpoints=${HOST_1}:2379,${HOST_2}:2379,${HOST_3}:2379 member list
```