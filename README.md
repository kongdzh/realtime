# realtime
sth changed

1.git clone // 到本地
2.git checkout -b xxx 切换至新分支xxx
（相当于复制了remote的仓库到本地的xxx分支上
3.修改或者添加本地代码（部署在硬盘的源文件上）
4.git diff 查看自己对代码做出的改变
5.git add 上传更新后的代码至暂存区
6.git commit 可以将暂存区里更新后的代码更新到本地git
7.git push origin xxx 将本地的xxxgit分支上传至github上的git
-----------------------------------------------------------
（如果在写自己的代码过程中发现远端GitHub上代码出现改变）
1.git checkout main 切换回main分支
2.git pull origin master(main) 将远端修改过的代码再更新到本地
3.git checkout xxx 回到xxx分支
4.git rebase main 我在xxx分支上，先把main移过来，然后根据我的commit来修改成新的内容
（中途可能会出现，rebase conflict -----》手动选择保留哪段代码）
5.git push -f origin xxx 把rebase后并且更新过的代码再push到远端github上
（-f ---》强行）
6.原项目主人采用pull request 中的 squash and merge 合并所有不同的commit
----------------------------------------------------------------------------------------------
远端完成更新后
1.git branch -d xxx 删除本地的git分支
2.git pull origin master 再把远端的最新代码拉至本地

记这些也没啥用，实习项目一实操都会了，
诸如什么无相关拉取的--allow-unrelated-histories,
日志查看最后提交，撤回，
修改message的git show/git log -n1 -p/git commit --amend --only/git rm --cached....，
暂存git stahs,出栈git stash pop等等谁记得啊，
还有讨论用rebase和merge的哪个顺手的，公共分支的谁给你用rebase，都是私有分支用，rebase变基一条线看起来舒服，但是协同开发出问题了要梳理就不那么舒服了，
merge就很清楚分支合并，都是推荐这样操作，
还有就是看你分支命名规范和提交日志的命名规则等等都能看出你的代码修养和工作经验。