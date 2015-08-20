title: python中的requests使用
date: 2015-08-06 17:13:53
categories: [笔记]
tags: [python, requests]
---
#1. 安装Requests
请移步[官网](http://www.python-requests.org/en/latest/user/install/#install)
我采用最土的方法，在`Lib\requests`路径下执行：
```bash
$ python setup.py install
```
---
#2. 发送请求
由于用了代理服务器，代理需要使用`HTTP Basic Auth`，可以使用 `http://user:password@host/`语法
```python
import requests

proxies = {
    "http": "http://user:password@ip:port/",
}

r = requests.get("http://iwangchen.com", proxies=proxies)
print(r.text)
```
---
#3. 安装bs4
请移步[官网](http://www.crummy.com/software/BeautifulSoup/bs4/download/4.4/)

备注一下：
`\Python34\Tools\Scripts\2to3.py`可将python2的程序转换为python3
```bash
$ 2to3.py -w bs4 xx.py
```