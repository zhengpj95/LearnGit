# Learn git

学习Git

学习Git与GitHub的配置

学习在Git下，编程，并保存到远程仓库GitHub中

**Try my best.**

## 常用命令

- git init
- git config --global user.name 'your name'
- git config --global user.email 'you email'
- git clone url
- git status
- git add .
- git add filename
- git commit -m 'description'
- git commit -am 'description'
- git rm xxx
- git mv name1 name2
- git log   //不显示已经删除的
- git log -n  //查看n条
- git log --pretty=oneline // 只显示版本号和备注信息
- git reflog  //可以查看已经删除的记录
- git reflog -n //查看n条
- git diff
- git diff --cached
- git diff HEAD^
- git remote add origin url
- git branch   //显示全部分支
- git branch newBranchName  //新建分支
- git branch -D branchName || git branch --delete branchName  //删除本地分支
- git push origin --delete branchName  //删除远程分支名
- git switch branchName //切换分支
- git stash
- git stash list

### remote

git remote -v

git remote remove origin

git remote add origin master [url]

设置默认的push远程仓库(origin: 原创仓库本地名称，master：远程仓库分支名)
git push --set-upstream origin master

```shell
git remote add github github-url
git remote add gitee gitee-url

git push github master
git push gitee master
```

### 自定义命令简称

```shell
git config --global alias.st status
git config --global alias.ci commit
git config --global alias.cm '!f() { git add -A && git commit -m "$@"; }; f'
```

### 操作全局配置

```shell
# 查看所有全局配置
git config --global --list

# 查看所有配置
git config --list

# 删除全局配置
## 终端执行命令：
git config --global --unset user.name
## 编辑配置文件：.gitconfig
git config --global --edit
```
