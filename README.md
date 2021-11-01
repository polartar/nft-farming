# NFT Yield Farming on BSC

***
## 【Introduction of the NFT Yield Farming on BSC】
- This is a smart contract that enable a user to farm yield by staking LP tokens (BEP20) into a NFT pool.
  - Once a user stake LP tokens into a NFT pool, reward token (Governance Token) are mined every block.
  - User who staked can receive the Governance Tokens as rewards (as farmed-yield) when that user un-stake.
- This smart contract works on BSC (Binance Smart Chain).

&nbsp;

***

## 【Workflow】
- Diagram / Workflow  
![【Diagram】NFT Yield Farming on BSC](https://user-images.githubusercontent.com/19357502/108629603-1888a900-74a4-11eb-9337-581f757d7b4c.jpg)

&nbsp;

***

## 【Setup】
### ① Install modules
- Install npm modules in the root directory
```
$ npm install
```

<br>

### ② Add `.env` to the root directory.
- Please copy code of `.env.example` into your `.env` 
  (Then, please input your information of wallets, private keys, etc... by following code of `.env.example` )

<br>

### ③ Compile contracts (on BSC testnet)
```
$ npm run compile:bsc-testnet
```

<br>

### ④ Test
- Execute test of the smart-contracts (on the BSC testnet)
  - [Note]: Sometime, timeout happen on this test. So I recommend that you try `⑤ Script` below instead of this test.   
```
$ npm run test:nft-yield-farming_bsc-testnet
($ truffle test ./test/test-bsc/NFTYieldFarmingOnBSC.test.js --network bsc_testnet)
```

<br>

### ⑤ Script
- Execute script of the smart-contracts on the BSC testnet (with `truffle exec` command)
```
$ npm run script:nft-yield-farming_bsc-testnet
($ truffle exec ./scripts/script-bsc/NFTYieldFarmingOnBSC.script.js --network bsc_testnet)
```
(※ Note: In advance, please check whether your deployer' wallet address on BSC testnet has enough BNB balance or not)

