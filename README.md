# 常用git命令总结
git是世界上最流行的分布式版本控制系统

【基础】
1. git init    将一个文件夹变成git仓库
2. git add <文件>    将修改添加到暂存区
3. git commit -m <描述>   将修改提交到git仓库
4. git status   查看仓库状态
5. git diff     查看工作区与暂存区/仓库的不同（暂存区里有东西就优先和暂存区diff）

【版本切换】
6. git log      查看从最近版本到最远版本的提交日志(不能查比当前更高的版本)
7. git reset --hard HEAD^/上一版本号   回退到某版本（HEAD当前本报；HEAD^^上上版本；HEAD~100上100版本）
8. git reflog   记录历史命令(可以查到每一步操作的版本号)
9. git diff HEAD -- <文件>  查看工作区和仓库最新版本的不同
10. git checkout -- <文件>  丢弃还未放入暂存区的工作区的修改
11. git reset HEAD <文件>   把暂存区的内容撤销，重新放回工作区
- 11 10两个命令可以组合使用（把暂存区里的修改内容全部撤销）
12. rm <文件>;   git rm <文件>;   git commit -m   删除文件组合操作

【远程仓库】
13. git remote add origin git@server-name:path/repo-name.git    关联远程仓库
14. git push -u origin master   第一次推送master分支所有内容，以后推送则不用加-u
15. git clone git@github.com:<远程路径>     ssh协议克隆远程仓库


参考文献：https://www.liaoxuefeng.com/wiki/896043488029600
