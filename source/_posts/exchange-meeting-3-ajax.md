---
title: SysLab技术分享-Vol.03—Ajax
date: 2016-05-12 20:44:32
tags: [交流会,前端]
author: ghostwolfs
---

HTTP请求

	一个完整的HTTP请求过程，通常有下面7个步骤：
		1.建立TCP连接
		2.web浏览器向web服务器发送请求命令
		3.web浏览器发送请求头信息
		4.web服务器应答
		5.web服务器发送应答头信息
		6.web服务器向浏览器发送数据
		7.web服务器关闭TCP连接
	一个HTTP请求一般由四部分组成：
		1.HTTP请求的方法或动作，比如是GET还是POST
		2.正在请求的URL
		3.请求头，包含一些客户端环境信息，身份验证信息等
		4.请求体，也就是请求正文

<!--more-->

GET：一般用于信息获取,使用url传递参数

		对所发送的信息的数量也有腌制，一般在2000个字符
POST：一般用于修改服务器上的资源.

		对所发送信息的数量无限制

HTTP相应一般由三个部分组成：

	1.一个数字和文字组成的状态码，用来显示请求是成功还是失败
	2.响应头，响应头也和请求头一样包含许多有用的信息，例如服务器类型，日期时间，内容类型和长度等
	3.响应体，也就是响应正文

HTTP状态码由三位数字构成:

	1xx : 信息类，表示收到web浏览器请求，正在进一步的处理中
	2xx : 成功，表示用户请求被正确接受，理解和处理。例如 200
	3xx : 重定向，表示请求没有成功，客户必须采取进一步的动作
	4xx : 客户端错误，表示客户端提交的请求有错误。例如 404
	5xx : 服务器错误，表示服务器不能完成对请求的处理。例如 500

XMLHttpRequest发送请求

	open(method,url,async)
	send(string)

XMLHttpRequest取得响应

	responseText : 获得字符串形式的响应数据
	responseXML  : 获得XML形式的响应数据
	status和statusText : 以数字和文本形式返回HTTP状态码
	getAllResponseHeader() : 获取所有的响应报头
	getResponseHeader() : 查询响应中的某个字段的值
	readyState属性:
		0 : 请求未初始化,open还没有调用
		1 : 服务器连接已建立,open已经调用了
		2 : 请求已接受,也就是接收到头信息了
		3 : 请求处理中,也就是接收到响应主体了
		4 : 请求已完成,且响应已就绪,也就是响应完成了

JSON基本概念

	JSON : JavaScript对象表示法(JavaScript Object Notation)
	JSON是存储和交换文本信息的语法,类似XML。它采用健值对的方式来组织,易于人们阅读和编写,同时也易于机器解析和生成
	JSON是独立于语言的,也就是说不管什么语言,都可以解析JSON,只需要按JSON的规则来就行

JSON与XML比较

	json长度短
	json读写的速度更快
	json可以用js直接解析
	JSONLint校验json的在线工具

Github地址: https://github.com/ghostwolfs/ajax-demo
