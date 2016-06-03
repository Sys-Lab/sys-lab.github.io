---
title: SysLab技术分享-Vol.01—代码规范相关
date: 2016-03-20 20:13:38
tags: [交流会,代码规范,项目流程]
description: 主要分享关于代码规范和开发流程相关的东西
author: Yasic Yu
---

## 1. 文档

 - 需求文档
 - 开发文档
 - TAB个数，4个还是8个，为了git审核

 - 变量命名
  - 匈牙利命名
  - 第一个字母定义变量类型
  - mUserId，m表示成员变量，i表示整型变量
  - 主要用在C和C++
  - 小驼峰

第一个单词首字母小写，其他首字母大写
大驼峰

全单词首字母大写
变量命名不能用拼音

方法命名

驼峰命名

get，set
Restful命名方式

资源状态转化
杜绝用动词
loopback--nodejs的restful框架
花括号换行

C和C++一般要换行
开发规范定好
JS不换行

<!--more-->

# 2. GIT COMMIT规范

Add XXX
fix #1234
modify XXXX
delete XXXX

# 3. 代码TIPS

注释

尽量少写注释
魔数问题
用英文写注释
空行

适当使用空行
一个函数内不同功能块空一行
便于阅读代码
DRY原则

Do not Repeat Yourself，不要复制和重复代码
如果需求类似，提出来做成一个单独的function
For循环迭代

先写迭代for循环，再补充循环变量
语法提示插件
# 4. 单元测试

测试便于检查代码
# 5. GIT FLOW

leader建主仓库
开发人员fork到自己名下
从自己仓库下载到本地
本地push到自己仓库
提交Pull Request
leader审核测试代码，merge进入主仓库
也可以用分支代替
