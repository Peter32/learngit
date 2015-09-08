Git is a version control system.
Git is free software.


Git is a distributed version control system.



# 首先，选择一个合适的地方，创建一个空目录：
$ mkdir learngit
$ cd learngit
$ pwd

# 第二步，通过git init命令把这个目录变成Git可以管理的仓库：
$ git init

git add readme.txt

git commit -m " first txt file"
git status

git diff readme.txt

# 为什么Git添加文件需要add，commit一共两步呢？因为commit可以一次提交很多文件，所以你可以多次add不同的文件
# 回退 当前版本是HEAD ,上一版本  HEAD^, 上上一版本HEAD^^

$git reset --hard HEAD^

#看看readme.txt的内容是不是版本
$ cat readme.txt

# git log --pretty=oneline

# 我的没有看到所有commit log, git log 失败
$ git reflog


为什么Git比其他版本控制系统设计得优秀，因为Git跟踪并管理的是修改，而非文件。

# Git会告诉你，git checkout -- file可以丢弃工作区的修改：

$ git checkout -- readme.txt

# 用命令git reset HEAD file可以把暂存区的修改撤销掉（unstage），重新放回工作区
$ git reset HEAD readme.txt


#git rm用于删除一个文件。如果一个文件已经被提交到版本库，那么你永远不用担心误删，但是要小心，你只能恢复文件到最新版本，你会丢失最近一次提交后你修改的内容。

$ git rm test.txt


要关联一个远程库，使用命令git remote add origin git@server-name:path/repo-name.git；

关联后，使用命令git push -u origin master第一次推送master分支的所有内容；

此后，每次本地提交后，只要有必要，就可以使用命令git push origin master推送最新修改；
