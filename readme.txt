Git is a version control system.
Git is free software.

首先使用git init将仓库变为git 仓库

对仓库中的代码进行修改

使用git add <file>把修改部分添加到暂存区域

使用git commit -m <message>提交修改（-m：添加修改说明）
例如：git commit -m "wrote a readme file"

使用git status命令可以让我们时刻掌握仓库当前的状态

使用git diff顾名思义就是查看difference

想要回退版本：
使用 git log查看提交历史，确定要退回到哪个版本
使用 git reset --hard HEAD~n（退回到n个版本前）

想要重返未来：
使用 git reflog查看命令历史，以便确定要回到未来哪个版本
使用 git reset --hard commit_id(输入想回到的版本)

想撤销修改：
使用 git checkout -- file 来把file在工作区的修改全部撤销

将本地库发送到github上：
使用 git remote add origin git@github.com:dondon03-10/learngit.git（ssh）与本地库进行关联(远程库的名字叫origin)
 
使用 git push -u origin master 将本地仓库的主支master发送到远程库上（-u是将本地主分支和远程的主分支直接关联起来）
后续进行远程推送使用 git push origin master 即可

使用 git pull origin master 获取远程仓库的最新代码

分支管理：
使用 git branch dev 创建分支
使用 git checkout dev 切换分支（git switch -c <name>也可以）

使用 git branch 查看当前分支

使用 git merge dev 将当前分支合并到master(需要切换到master上再使用，合并对象默认为当前所在分支)

使用 git branch -d dev 删除分支

创建、合并和删除分支非常快。跟直接在master上工作一样，但是过程更安全


标签管理：
使用 git tag <name> 给一个分支打标签

打上标签可以方便管理各项目分支版本


使用git rebase -i HEAD~n 可以从最开始往后删n个版本，可以有助于减少git push上传量，或将敏感信息删除