Git is a distributed version control system.
Git is free software  distributed under the GPL.
Git has a mutable index called stage.
Git tracks changes.
/////////////////////////
The first time use git.
09-29
your brunch is ahead of 'origin/master' by 1 commit. //就是本地仓库有一个提交，比远程仓库要先进一个commit。git push origin master之后，再用git staus

用HEAD表示当前版本--本地？

多个版本(commit)切换----是每个版本都被保存下来了？

因为Git在内部有个指向当前版本的HEAD指针

git reflog用来记录你的每一次命令


工作区/暂存区 ：Git和其他版本控制系统如SVN的一个不同之处就是有暂存区的概念。
 工作区有一个隐藏目录.git，这个不算工作区，而是Git的版本库。

 因为我们创建Git版本库时，Git自动为我们创建了唯一一个master分支，所以，现在，git commit就是往master分支上提交更改

 untracked 还没被git add 

 git diff HEAD -- readme.txt命令可以查看工作区和版本库里面最新版本的区别