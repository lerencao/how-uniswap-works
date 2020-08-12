---
marp: true
theme: gaia
footer: by [lerencao](https://github.com/lerencao)
paginate: true
---
<!--
_class: lead invert
_paginate: false
 -->

# Uniswap 介绍


- 心智模型
- 做市
- 交易
- 费用
- Price Oracle
- 优缺点

---
<!--
class: lead invert
-->

## 心智模型

- 传统交易所：挂单/吃单
- uniswap：自动做市商（AMM）
  - 底池/底仓/Pool
  - 流动性/Liquidity
  - 交易/Trade/Swap

---

<!--
_class: lead invert
-->
![width:30cm](https://uniswap.org/static/402f9d4fd5e78d4a7977a938e69343f2/df51d/anatomy.jpg)

**恒定乘积模型**

``` ruby
# before:             # after:
x * y = k     ==>     (x + a) * (y - b) = k
```

---


## 做市 (aka 提供流动性)

![width:30cm](https://uniswap.org/static/94f9a497b001a6b27df2c37adadc05b4/824f2/lp.jpg)

- 流动性越高，价格滑动越缓慢。

---

## 交易

![width:30cm](https://uniswap.org/static/40a3fe965d188286abe8502f68ef42a1/4eea2/trade.jpg)

---


## 费用

- trading fee: 0.3%
- slipping rate.
- protocol fee: 1/6 of trading fee. (for developers, not enabled for now)

---

## 价格 oracle

![height:16cm](https://uniswap.org/static/305e79bfff0602175a5d2948fc4a820d/97a96/v2_onchain_price_data.png)


---

![width:30cm](https://uniswap.org/static/f134d0d4763a11354a400c3c944aecad/97a96/v2_twap.png)

---

## 和 cex 比较

- cex: 深度不够，容易砸盘。
- dex:
  - 只适用于想*市价交易*的用户，不适用于*限价交易*的用户。
  - 交易费比较高。
  - 做市商需要承受 *impermanent loss*。


---

## 参考

- [uniswap doc](https://uniswap.org/docs/v2/)
- [uniswap paper](https://uniswap.org/whitepaper.pdf)
- [cex and dex](https://www.lichang.io/articleDetail/563924)
- [impermanent loss](https://uniswap.org/docs/v2/advanced-topics/understanding-returns/)