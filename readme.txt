-------版本库-------
把工作区的文件添加到暂存区
git add readme.txt xxx.txt

把暂存区的所有内容提交到当前分支
git commit -m "wrote a readme file"

查看仓库状态
git status

如果status有变化，查看具体变化 （工作区和版本库里最新版本的区别）
git diff


-------时光机-------


1. 回退版本
git reset --hard HEAD^
--hard  回退到版本的已提交状态
--soft  回退到版本的未提交状态
--mixed 回退到版本的已添加未提交状态
HEAD^^  上上个版本
HEAD～7  7个版本前

查看提交历史，以便确定要回退到过去的哪个版本
git log

查看命令历史，以便确定要回退到未来的哪个版本
gitreflog

2. 工作区和暂存区
工作区 (Working Directory)
版本库 (Repository) .git
暂存区 (stage/ index) .git中

3. 撤销修改

5. 删除文件


