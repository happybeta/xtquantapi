# XtQuant
迅投QMT接口相关介绍和常用功能封装，详细文章介绍请移步公众号

## 目录

- [XtQuant](#xtquant)
  - [目录](#目录)
  - [初探迅投QMT极简策略系统](#初探迅投qmt极简策略系统)
  - [行情接口分析](#行情接口分析)
    - [行情接口以及历史行情数据下载](#行情接口以及历史行情数据下载)
    - [历史行情批量缓存](#历史行情批量缓存)
    - [历史行情转存数据库](#历史行情转存数据库)
  - [交易接口分析](#交易接口分析)
    - [交易接口封装](#交易接口封装)
  - [量化策略研究](#量化策略研究)
    - [新闻事件量化](#新闻事件量化)
    - [技术面特征提取](#技术面特征提取)
  
----

## 初探迅投QMT极简策略系统
[初探迅投QMT极简策略系统](https://mp.weixin.qq.com/s/5XI09nyStjmD0faYs9UIlw) 迅投QMT是一个门槛相对较低、功能强大的量化策略交易系统。本文首先介绍一些背景知识，并主要分析极简策略交易系统的一些功能，后续将陆续分享行情、交易、策略等相关实战教程。

## 行情接口分析

### 行情接口以及历史行情数据下载
[行情接口以及历史行情数据下载](https://mp.weixin.qq.com/s/R2WquJUD4Mu6wuoFjoC3AQ) :本文主要介绍QMT行情接口概况和一个历史行情数据下载案例

### 历史行情批量缓存
[历史行情批量缓存](https://mp.weixin.qq.com/s/l-pFVnqsWjLP1iBM63dD9Q) :本文进一步介绍如何获取批量股票代码并缓存对应的tick、分钟、日级别的历史数据。

### 历史行情转存数据库
[迅投QMT历史行情转存Clickhouse数据库](https://mp.weixin.qq.com/s/5337pliFLRlpQoEkQA31Og): 本节介绍如何将读取本地的缓存数据并写入到clickhouse数据库中。历史行情数据从格式上看分为tick数据和K线数据两大类，针对这两类的数据我们分别处理。

## 交易接口分析

### 交易接口封装
[迅投QMT量化平台交易接口封装](https://mp.weixin.qq.com/s/42ixWcqA0k71Xr49BbzrIg): 迅投QMT量化平台提供了极简客户端，可直接使用Python调用其提供的交易功能。本文使用Python中的Sanic异步框架将交易接口进一步封装成HTTP访问接口，方便从远程Linux主机调用。

源码：`src/trade_service.py`


## 量化策略研究

### 新闻事件量化
[基于新闻事件Bert序列建模的行业涨跌预测](https://mp.weixin.qq.com/s/CJxhVB6m2-DINp1mGNL4Bw): 利用先进的深度学习技术单独分析新闻事件序列对行业指数的短期影响，和读者一起探讨利用AI做行业选股的可行性。

### 技术面特征提取
[利用pandas_ta自动提取技术面特征](https://mp.weixin.qq.com/s/PPduk4xPcix9USW9HmUpHw) TA-Lib是一个技术分析库，涵盖了150多种股票、期货交易软件中常用的技术分析指标，如MACD、RSI、KDJ、动量指标、布林带等等，而pandas-ta则是一个基于pandas和ta-lib的高级技术分析工具，具有130多个指标和实用功能以及60多个TA-Lib中包含的蜡烛模式。本章节记录如何利用pandas-ta快速提取技术面特征。

---

欢迎关注我的公众号“**量化实战**”，原创技术文章第一时间推送。

![公众号](misc/qrcode.jpg)
