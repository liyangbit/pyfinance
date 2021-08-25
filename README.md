- [01 微信公众号文章代码文件列表](#01-微信公众号文章代码文件列表)
- [02 部分内容介绍](#02-部分内容介绍)
  - [财经工具 Tushare 介绍](#财经工具-tushare-介绍)
    - [使用 Tushare](#使用-tushare)
  - [用Python制定投资计划](#用python制定投资计划)
  - [用 Python 快速追踪基金的收益情况](#用-python-快速追踪基金的收益情况)

主要分享 Python 在财经领域的一些实践。

---

**风险提示：** 仓库内容主要目的是给大家分享 Python 在财经领域的应用，文中提到的品种或标的，仅作为文中技术实现之用。投资有风险，入市需谨慎，文中内容不构成投资建议，抄作业请理性分析市场。

---
# 01 微信公众号文章代码文件列表

欢迎关注个人微信公众号“**Python数据之道**”（公号ID：**PyDataLab** ）。

<div align="center">
    <img src="./03image/QR-Python数据之道.jpg" width="200"/>
</div>

微信公众号上目前已发布的部分文章链接，以及对应的代码或数据文件如下：

|文章发布日期|文章名称及链接|代码 / 数据文件|
|-------|---------|---------|
|20210131|[财经数据神器 Tushare，股票数据全搞定](https://mp.weixin.qq.com/s/c1ukemeK12flCgA-lo69fA)|[请点击链接](https://github.com/liyangbit/PyDataRoad/tree/master/comprehensive/Tushare)|
|20210831|[用 Python 快速追踪基金的收益情况](http://liyangbit.com/)|[请点击链接](https://github.com/liyangbit/pyfinance/tree/main/01code) ，查找 `202108-mutual-fund.ipynb` 文件|


# 02 部分内容介绍

## 财经工具 Tushare 介绍

关于财经数据，有多个Python库可以供咱们选择，其中 tushare 是国内较早开始发布财经数据的社区，其内容比较完善，今天我们使用的就是 tushare 。

Tushare 是一个金融大数据平台，数据内容包含股票、指数、基金、期货、债券、外汇、行业大数据等，同时包括了数字货币行情等区块链数据，为各类金融投资和研究人员提供适用的数据和工具，概览如下：

<!-- ![tushare概览](https://tva1.sinaimg.cn/large/008eGmZEgy1gn3j7d8wnwj30is0ya45g.jpg)

全部内容很丰富，为了有助于大家有个整体的了解，阳哥绘制了一张完整的思维导图，截图如下： -->

![tushare思维导图](https://tva1.sinaimg.cn/large/008eGmZEgy1gn3r6vz09nj30u016r7mw.jpg)


### 使用 Tushare

Tushare 平台的数据，已全面升级到 tushare pro 了，通常情况下，还是称之为 tushare。

想使用 tushare 中的数据和功能，首先需要进行注册，获得一份 token （一串字母和数字组成的文本），然后才可以获取到数据，大家可以通过以下链接来注册：

[点击注册tushare](https://tushare.pro/register?reg=129033)

在 `tushare` 中注册后，通过 “个人主页”——“接口TOKEN” 可以找到自己的 token 值，界面如下：

<!-- ![tushare](images/posts/2020-04-27-plotly-txt/2.png) -->

![tushare接口TOKEN](https://tva1.sinaimg.cn/large/008eGmZEgy1gmwqwnfvdsj30l60b8aar.jpg)

复制 token 值，然后在代码中进行如下设置：

```python
# 设置 token
# tushare 注册地址： https://tushare.pro/register?reg=129033
# 以上方法只需要在第一次或者token失效后调用，完成调取tushare数据凭证的设置，正常情况下不需要重复设置。
ts.set_token('你的token值')

pro = ts.pro_api()
```

在设置好 token 值后，我们就可以开始获取数据。


关于 tushare 的详细介绍，请点击下面的链接前往：

- [神器Tushare，财经数据必备工具！](https://mp.weixin.qq.com/s/c1ukemeK12flCgA-lo69fA)

## 用Python制定投资计划

可以用 excel 或 Python 来制定单个标的的投资计划，相对来说，用 Python 制作的计划的复用性要好些。

效果如下：

[![2-Python表格](https://tva1.sinaimg.cn/large/008i3skNgy1gswp9l5g85j30oo0g276a.jpg)](https://mp.weixin.qq.com/s/1bmyG7LmXNUfXtFsb_mgnQ)

详细的实现过程，可以参考下面的内容“

- [用Python来做一个投资计划](https://mp.weixin.qq.com/s/WYuMwCJBrWaBiDs8xp2KMA)

## 用 Python 快速追踪基金的收益情况

用 Python 来追踪和更新基金的收益情况，涉及到的Python库主要是 pandas 和 tushare。

最终实现的效果如下：

![](https://tva1.sinaimg.cn/large/008i3skNgy1gtt3x6riggj60xi0u0wn802.jpg)

详细的实现过程，代码文件请点击下面链接，查找 `202108-mutual-fund.ipynb` 文件：

- [代码文件列表](https://github.com/liyangbit/pyfinance/tree/main/01code)
