# Description
This is the repo for TokenPocket to add public chains according to the community requirements. Once the PR is merged, the chain will be included on TokenPocket's Easy Add feature. Please read the following tutorials.

## Listing and donation standard
https://help.tokenpocket.pro/developer-en/network/add-chain

A donation is needed for your PR to be merged. If your PR is not compatible with the Review Rules, it won't be merged and the donation won't be refunded. Please be cautious.


# 简介
本仓库为TokenPocket根据社区需求进行自定义网络（公链）更新，只要PR被合并就可以在自定义网络--快捷加链的列表中收录，请根据以下指引进行提交。

## 公链收录审核及捐赠标准
https://help.tokenpocket.pro/developer-cn/public-chain/add-chain

提交PR合并需要捐赠,如果不满足审核要求，则不进行合并，捐赠不会进行退回，请您按需进行提交。

## How to add a new chain

Fork this repo and add your evm chain info into `chains.json` 

Example:

```javascript
{
    "name": "xDAI Chain",
    "chainId": 100,
    "shortName": "xdai",
    "chain": "XDAI",
    "network": "mainnet",
    "networkId": 100,
    "nativeCurrency": {
        "name": "xDAI",
        "symbol": "xDAI",
        "decimals": 18
    },
    "rpc": [
        "https://rpc.xdaichain.com",
        "https://xdai.poanetwork.dev",
        "wss://rpc.xdaichain.com/wss",
        "wss://xdai.poanetwork.dev/wss",
        "http://xdai.poanetwork.dev",
        "https://dai.poa.network",
        "ws://xdai.poanetwork.dev:8546"
    ],
    "faucets": [],
    "infoURL": "https://forum.poa.network/c/xdai-chain",
    "app_resource": {
        "ic_chain_select": "https://tp-upload.cdn.bcebos.com/v1/blockChain/xDAI/1.png",
        "ic_chain_unselect": "https://tp-upload.cdn.bcebos.com/v1/blockChain/xDAI/0.png",
        "color_chain_bg": "0x58B2AF"
    }
    "chain_metadata": {
        "balance_source": 1, // 获取余额的方式，0是从服务器获取，1是从节点获取
        "balance_contract": "0xb1f8e55c7f64d203c1400b9d8555d050f94adf39", //批量查询余额合约
        "balance_url": "", //获取余额接口链接
        "tx_url": "https://pretxs.mytokenpocket.vip", //获取交易记录接口链接
        "multi_sig": {
            "singleton": "0x3e5c63644e683549055b9be8653de26e0b4cd36e",
            "factory": "0xa6b71e26c5e0845f74c812102ca7114b6a896ab2",
            "callback": "0x08471d9d2099a8Cf55F5f1Ee77291a3CE9A0B021",
            "compatibilityFallbackHandler": "0xf48f2B2d2a534e402487b3ee7C18c33Aec0Fe5e4",
            "channels": {
                "android": "1.6.3",
                "ios": "1.9.1",
                "extension": "1.1.11"
            }
        }
    }
}
```

## 如何添加一个新链

Fork该仓库并在`chains.json` 中加入您的EVM链信息

示例:

```javascript
{
    "name": "xDAI Chain",
    "chainId": 100,
    "shortName": "xdai",
    "chain": "XDAI",
    "network": "mainnet",
    "networkId": 100,
    "nativeCurrency": {
        "name": "xDAI",
        "symbol": "xDAI",
        "decimals": 18
    },
    "rpc": [
        "https://rpc.xdaichain.com",
        "https://xdai.poanetwork.dev",
        "wss://rpc.xdaichain.com/wss",
        "wss://xdai.poanetwork.dev/wss",
        "http://xdai.poanetwork.dev",
        "https://dai.poa.network",
        "ws://xdai.poanetwork.dev:8546"
    ],
    "faucets": [],
    "infoURL": "https://forum.poa.network/c/xdai-chain",
    "app_resource": {
        "ic_chain_select": "https://tp-upload.cdn.bcebos.com/v1/blockChain/xDAI/1.png",
        "ic_chain_unselect": "https://tp-upload.cdn.bcebos.com/v1/blockChain/xDAI/0.png",
        "color_chain_bg": "0x58B2AF"
    }
}
```



`app_resource` is optional, which is only affect the appearance in TokenPocket Wallet. You can follow the standard below:


![standard](https://tp-statics.tokenpocket.pro/images/custom-chains-standard-11.png)
![standard](https://tp-statics.tokenpocket.pro/images/custom-chains-standard-12.png)
![standard](https://tp-statics.tokenpocket.pro/images/custom-chains-standard-13.png)
![standard](https://tp-statics.tokenpocket.pro/images/custom-chains-standard-14.png)
![standard](https://tp-statics.tokenpocket.pro/images/custom-chains-standard-15.png)

