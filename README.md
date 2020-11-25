# 以太坊Go源码分析

## 以太坊的架构
以太坊的架构设计可以简单的分为三个层次，协议层、接口层和应用层。而协议层又可以分为网络层和存储层。

## 源码的目录结构

```
|---accounts                以太坊账户管理
|---build                   主要是编译和构建的一些脚本和配置
|---cmd                     命令行工具
|     |---abigen            合约接口生成工具
|     |---bootnode          实现网络发现的节点
|     |---evm               以太坊虚拟机
|     |---faucet
|     |---geth              以太坊命令行客户端
|     |---p2psim            提供了一个工具来模拟http的API
|     |---puppeth           创建一个新的以太坊网络的向导
|     |---rlpdump           提供RLP数据的格式化输出
|     |---swarm             swarm网络的接入点
|     |---util              公共的组件
|     |---wnode             这是一个简单的Whisper节点。 它可以用作独立的引导节点。此外，可以用于不同的测试和诊断目的。
|---common                  提供了一些公共的工具类
|---consensus               以太坊的共识算法，包括ethhash, clique
|---console
|---contract
|---core                    以太坊的核心数据结构和算法(虚拟机，状态，区块链，布隆过滤器)
|---crypto                  加密,数字签名和hash算法
|---docs
|---eth                     实现了以太坊的协议
|---ethclient               以太坊的RPC客户端
|---ethdb                   eth的数据库,主要是LevelDB及相应接口
|---ethstats
|---event                   实时事件处理
|---graphql
|---internal
|---les
|---light                   实现为以太坊轻量级客户端提供按需检索的功能
|---log
|---metrics                 提供磁盘计数器
|---miner                   以太坊的挖矿和共识算法
|---mobile                  移动端使用的一些warpper
|---node                    以太坊的多种类型的节点
|---p2p                     以太坊p2p网络协议
|---rlp                     以太坊序列化和反序列化处理
|---rpc                     远程方法调用
|---singer
|---swarm                   swarm网络处理
|---tests
|---trie                    以太坊重要的数据结构MPT的实现
```