# ethereum-oracle-service
以太坊Oracle后端服务

[《撸一个预言机（Oracle）服务，真香！》系列文章](https://www.jianshu.com/c/4b0a4137dcb8)

## 1、编译
```
go build
```
编译完成后查看帮助信息

```
./oracle-service -h
oracle_service version: 1.0.0
Usage: oracle_service [-h help] [-v version] [-c config path] [-l log path]
```
## 2、配置

配置信息如下：

```
# 合约地址
OracleContractAddress = ""
# 网络ws地址
NetworkWS = "ws://"
# 调用合约的私钥
PrivateKey = ""
```

## 3、运行
```
./oracle-service -c ./conf/app.conf -l logs/
```

##注意事项
1>
1.先部署合约 并设置合约费用
2.将合约地址和owner地址填入
3.获取ws地址 填入文件
4.注释log初始化
5.启动
2>

1.先部署oracle合约
2.再部署调用合约 合约完整的返回请求值 不做处理或者做处理后解决。

3>调试
remix 
remixd -s /Users/houzi/remix/ --remix-ide https://remix.ethereum.org

4>ide问题
Cannot identify version of git executable: no response – on startup
删除缓存重启
