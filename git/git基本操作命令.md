# git基本操作命令

[TOC]

## git init

初始化一个仓库

```
git init
```

## git clone

从现有的git仓库中克隆一个仓库

```
git clone <repo>
```
```
git clone <repo>:<directory>
```

```
git clone git@github.com:hb951396063/PersonalNotes.git
```

## git add

把修改好的文件添加到缓存区

```
git add README.MD hello.py 加入多个文件
```

```
git add . 把所有文件都加入缓存区
```

## git rm

把缓存区的某个文件删除掉，不提交至仓库中

```
git rm -r --cached .DS_Store
git commit -m 'delete .DS_Store' 
```

## git status

查看git项目当前状态

```
git status
```

```
git status -s 以简短的形式输出结果
```

## git diff

查看执行git status的结果的具体信息

```
git diff
```

## git commit

git add将内容写入缓存区，git commit则将缓存区的内容添加到仓库中

```
git commit -m '提交的信息内容'
```

## git reset HEAD

该命令用于取消已经缓存的内容

```
git reset HEAD hello.py
```

## git branch

分支管理必杀技。无参数时，会list出所有的本地分支，有参数则是创建一个新的分支

```
git branch 罗列本地的分支情况
```

```
git branch <branch_name> 创建新分支
```
```
git branch -d <branch_name> 删除分支内容
```



## git checkout

切换分支

```
git checkout <branch_name> 切换一个已经存在的分支
```

```
git checkout -b <branch_name>新建一个分支并切换到该分支上
```

## git merge

将分支内容合并到主分支

```
git merge <branch_name>
```

## git log

查看git提交历史

```
git log
git log --oneline 简洁展示版本
git log --reverse 逆向展示所有日志（推荐使用）
git log --decorate 展示标签信息
```

## git tag

创建快照标签

```
git tag 展示所有的tag列表
```

```
git tag -a <tag_name> <branch_id> -m <tag_message>
```

## git fetch

从远端仓库下载新分支与数据

```
git fetch
```

## git merge

从远端仓库提取数据并尝试合并到当前分支

```
git merge
```

## git pull

从远端仓库获取最新版本并merge到本地

```
git pull origin master    //相当于git fetch 和 git merge
```

注:用git pull更新代码的话就比较简单暴力了但是根据commit ID来看的话，他们实际的实现原理是不一样的，所以不要用git pull，用git fetch和git merge更加安全。

<https://www.cnblogs.com/jing-tian/p/11154485.html>

## git push

将本地 [branch] 分支推送成为 [alias] 远程仓库上的 [branch] 分支

```
git push [alias] [branch]
```

