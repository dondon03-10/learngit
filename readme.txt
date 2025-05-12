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
