
欢迎来到 bos-testnet

[View in English](README.md)

## docker images 
You should update the last version from https://hub.docker.com/r/boscore/bos/tags/

### 克隆项目

```
git clone https://github.com/boscore/bos-testnet.git
cd fullnode
```

### 5秒之内搭建一个全节点

```
./run.sh
```

### 1分钟内手动搭建全节点

第一步，创建所需要的目录:

```
mkdir -p /data/eos/nodeos-data-volume/nodeos-data-bostest/data
```

第二步，准备配置文件:

```
cp -r config /data/eos/nodeos-data-volume/nodeos-data-bostest
```

第三步，启动全节点

```
docker-compose -f docker-compose-bostest-init.yaml up -d
```

### 暂停/重启 同步

暂停:

```
docker-compose -f docker-compose-bostest.yaml down
```

重启:

```
docker-compose -f docker-compose-bostest.yaml down
docker-compose -f docker-compose-bostest.yaml up -d
```
## 链信息

```
"chain_id": "33cc2426f1b258ef8c798c34c0360b31732ea27a2d7e35a65797850a86d1ba85"

```

## P2P 节点列表

```
p2p-peer-address = 120.197.130.116:9000
p2p-peer-address = 13.230.195.142:9866
p2p-peer-address = 120.197.130.117:9000
p2p-peer-address = 120.197.130.117:9001
p2p-peer-address = 120.197.130.117:9002
p2p-peer-address = 120.197.130.117:9003
p2p-peer-address = 45.79.145.205:9000
p2p-peer-address = 47.91.244.124:443
p2p-peer-address = 8.208.9.182:443
p2p-peer-address = 47.254.82.241:443
p2p-peer-address = 47.254.134.167:443
p2p-peer-address = 149.129.133.66:443
p2p-peer-address = 35.221.141.101:9878
p2p-peer-address = 35.221.141.101:9880
p2p-peer-address = 35.221.141.101:9900
p2p-peer-address = 35.236.174.234:9902
p2p-peer-address = 35.236.174.234:9903
p2p-peer-address = 35.236.174.234:9904
```


## HTTP API 节点列表

API nodes:
```
http://47.254.82.241:80/v1/chain/get_info 
http://47.254.134.167:80/v1/chain/get_info 
http://49.129.133.66:80/v1/chain/get_info 
http://8.208.9.182:80/v1/chain/get_info 
http://47.91.244.124:80/v1/chain/get_info
http://120.197.130.117:8020/v1/chain/get_info
```

支持 `get actions` ( filter-on=* ) 的API:
```
http://ap.testnet.bos.blockgo.pro
```

## 水龙头

在 `bos` 上创建账号非常简单:

#### 免费账号
创建免费账号: http://13.230.195.142/create_account?new_account_name

例子:
```
curl http://13.230.195.142/create_account\?111111111ooo
```

#### 获得免费Token
获得免费Token: http://13.230.195.142/get_token?your_account_name. 
每一次调用能获得100EOS, 每天最多获得1000个EOS.

例子:
``` 
curl http://13.230.195.142/get_token?111111111ooo
```

## 电报监控地址：
 https://t.me/bosteststatus 





