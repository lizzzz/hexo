title: 初识Git
date: 2014-12-01 10:57:35
categories: [笔记]
tags: [git, github]
---
学习`Git`的笔记，未完待续。

##创建版本库
---

将目录变成`Git`可以管理的版本库

```bash
$ git init
```

##把文件添加到版本库
---
把文件添加到版本库

```bash
$ git add <file>
```

把文件提交到版本库
可多次`add`，一次`commit`

```bash
$ git commit -m "wrote a readme file"
```

##版本库状态
---
仓库当前的状态

```bash
$ git status
```

查看`difference`

```bash
$ git diff
```

<!--more-->


##日志
---
显示从最近到最远的提交日志

```bash
$ git log
```

输出一行`log`信息

```bash
$ git log --pretty=oneline
3628164fb26d48395383f8f31179f24e0882e1e0 append GPL
ea34578d5496d7dd233c827ed32a8cd576c5ee85 add distributed
cb926e7ea50ad11b8f9e909c05226233bf755030 wrote a readme file
```

一大串类似`3628164...882e1e0`的是`commit id`，由`SHA1`计算。

每一次命令的记录

```bash
$ git reflog
```

##版本回退
---
在`Git`中，用`HEAD`表示当前版本，上一个版本就是`HEAD^`，上上一个版本就是`HEAD^^`，当然往上100个版本写100个^比较容易数不过来，所以写成 `HEAD~100`。

回退到某个版本

```bash
$ git reset <commit_id>
```

##撤销修改
---
将工作区的修改全部撤销

```bash
$ git checkout -- <file>
```

##丢弃本地修改 与最新版本同步
---

```bash
$ git reset --hard
$ git pull
```