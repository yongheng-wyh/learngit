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

 git checkout -- file 丢掉工作区的修改  --以版本库（暂存区|master）里为准
 git checkout file 没有-- 就是切换分支

 git reset HEAD file 把暂存区的修改撤销 重新放回工作区

 on branch master 
 your brunch is ahead of 'origin/master' by 5 commits.
 use 'git push' to publish your local commits

 ?? 1这个超前是指本地master 比 远程master吗？2关联的远程库是和本地库意义对应的吧



 远程仓库 以github为例

 创建SSH 
 $ ssh-keygen -t rsa -C "youremail@example.com"

 远程为什么要需要SSHkey  远程仓库如GitHub需要识别出你推送的提交确实是你推送的，而不是别人冒充的

 添加远程仓库

 在远程库创建一个新的仓库 -命名
 github告诉我们，可以从这个仓库克隆出新的仓库，也可以把一个已有的本地仓库与之关联，然后，把本地仓库的内容推送到GitHub仓库
 在本地的learngit仓库下运行命令：$ git remote add origin git@github.com:michaelliao/learngit.git （michaellia替换成自己的账户名）
 添加后，远程库的名字就是origin，这是Git默认的叫法

 把本地库的所有内容推送到远程库：$ git push -u origin master //本地master-->远程master分支 并关联
 把本地库的内容推送到远程，用git push命令，实际上是把当前分支master推送到远程。

 -u 第一次加，以后只要本地作了提交，就可以通过命令：$ git push origin master


从远程库克隆 git clone + 仓库地址
先创建远程库 /gitskills 添加内容 或者已有远程库
$ git clone git@github.com:michaelliao/gitskills.git 克隆到本地

git push origin yongheng  推到远程库里的 yongheng分支


//////
先clone 到本地 --本地有了一个master分支  git checkout  -b yongheng -b(创建新分支并且切换到这个分支) --在本地的master分支又拉了一个 yongheng分支  相当于git branch yongheng 再 git checkout yongheng？  


git upstream origin yongheng  关联了一个远程库的分支叫yongheng  


每次commit是 提交到本地的yongheng 分支 --master？ 自动同步到远程的 yongheng 分支


10-15