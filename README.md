# 哪些人是威胁者

通过 JS SDK 的方式判断哪些威胁者属于有害的访问者。通过分析网站访问者的元信息，并从这些访问者中找出哪些是有威胁的。

# 常见的威胁者名单
- 扫描器
- 爬虫
- 渗透测试软件
- 黑 IP

# 安装

参见站点： https://sdk.egoid.me

# 判别原理

通过云端与客户端双向监测的方式发现潜在的威胁。

## 前端 SDK

前端通过部署 SDK 采集需要的参数，云端通过分析采集的参数，从数据矩阵中发现其中恶意篡改的数据和常见的威胁特征数据；
前端通过一定的 JS 代码测试，检测浏览器特性，防御常见的无头和脚本访问。

## 云端分析

云端主要分析了 IP ，UA，HTTP 协议，SSL 协议等特征进行特征匹配，通过每日更新样本库的形式来实时判别恶意流量。

# 后续规划

如果该方案可以检测出大部分威胁者，将详细讲解检测实现思路，并通过开源的方式交流学习。

# Version 1.1 2019/6/26

- [x] 增加爬虫流量时段趋势报表
- [x] 增加 IP 风险查询接口，返回爬虫 IP 风险信息

![](./version-6-26/2019-07-10-16-10-40.png)
![](./version-6-26/2019-07-10-16-11-14.png)
