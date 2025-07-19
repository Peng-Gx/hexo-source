---
title: 了解git
date: 2025-07-19 18:54:05
tags:
---



### 使用git的目的
对于当前的我来说，使用git主要是为了使用github，将代码保存到远程仓库，并且记录每一次的提交内容以供回溯，涉及的仅是单分支的管理和同步。未来可能会涉及多个分支，以及各种回滚操作，但现在我还用不到。

### 怎么创建git仓库

#### 方法一
远程创建一个空仓库，本地初始化仓库，关联远程仓库，修改本地分支名，提交本地分支到远程仓库
```bash
git init 
git add .
git commit -m "message"
git branch -M main //改本地分支名字
git remote origin "git@xxx" //配置一个远程仓库，别名origin
git push -u origin main //将本地分支提交到远程仓库，没有对应名字分支则创建对应分支，也可以提交到不同名字的分支比如git push -u origin main:dev；这句语句之后本地分支和远程分支之间就会建立关联，直接push就是对应分支

//前面配置完，就可以使用这些语句进行简单的提交
git add .
git commit -m "message"
git push

```

#### 方法二
现在远程创建一个空仓库，然后clone到本地，把文件拷贝过去然后提交即可，其他操作都不需要
```bash
git add .
git commit -m "message"
git push
```

### 