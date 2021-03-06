## USDT钱包运维手册\MAID钱包运维手册

### [参考1：BTC比特币钱包运维手册](BTC.md)
`USDT和MAID是运行在BTC网络上的代币。`

#### USDT官网：  https://tether.to/
#### USDT区块浏览器： https://www.omniexplorer.info/asset/31
#### MAID区块浏览器： https://www.omniexplorer.info/asset/3

#### 支持主要币种有：USDT、MAID等

#### （1）Omni钱包安装
###### Omni钱包： http://www.omnilayer.org/
###### Omni钱包源码、BIN包： https://github.com/OmniLayer/omnicore

#### （2）Omni钱包启动
`./bin/omnicored -daemon -port=端口号 -conf=/home/user/.usdtcoin/bitcoin.conf -datadir=/home/user/.usdtcoin`

#### （3）Omni钱包配置文件:同比特币(bitcoin.conf)
```
testnet=0
txindex=1
server=1
rpcport=rpc端口号
rpcuser=账号
rpcpassword=密码
rpcallowip=127.0.0.1/32
gen=0
```

#### （4）[日常维护命令同比特币](BTC.md)
####
#### （5）查询USDT余额
`./bin/omnicore-cli -conf=/home/user/.usdtcoin/bitcoin.conf omni_getbalance 14FuhpJ9ixW5EyoXT1G21BAKgAvitx35pR 31`

#### （6）查询MAID余额
`./bin/omnicore-cli -conf=/home/user/.usdtcoin/bitcoin.conf omni_getbalance 14FuhpJ9ixW5EyoXT1G21BAKgAvitx35pR 3`

#### （7）转账USDT（先解锁钱包）
```
./bin/omnicore-cli -conf=/home/user/.usdtcoin/bitcoin.conf omni_funded_send "出款USDT地址" 
                        "收款USDT地址" 31 "金额" 
                        "手续费账号"
```

#### （8）转账MAID（先解锁钱包）
```
./bin/omnicore-cli -conf=/home/user/.usdtcoin/bitcoin.conf omni_funded_send "出款MAID地址" 
                        "收款MAID地址" 3 "金额" 
                        "手续费账号"
```
