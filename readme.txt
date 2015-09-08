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