-------版本库-------
把工作区的文件添加到暂存区
$ git add readme.txt xxx.txt

把暂存区的所有内容提交到当前分支
$ git commit -m "wrote a readme file"

查看仓库状态
$ git status

如果status有变化，查看具体变化 （工作区和版本库里最新版本的区别）
$ git diff


-------时光机-------


1. 回退版本
$ git reset --hard HEAD^
--hard  回退到版本的已提交状态
--soft  回退到版本的未提交状态
--mixed 回退到版本的已添加未提交状态
HEAD^^  上上个版本
HEAD～7  7个版本前

查看提交历史，以便确定要回退到过去的哪个版本
$ git log

查看命令历史，以便确定要回退到未来的哪个版本
$ gitreflog

2. 工作区和暂存区
工作区 (Working Directory)
版本库 (Repository) .git
暂存区 (stage/ index) .git中

3. 撤销修改
把x文件在工作区的修改全部撤销
$ git checkout -- readme.txt

情况一：修改后还没有add到暂存区：修改回和版本库一模一样的状态
情况二：add到暂存区后又修改：修改回add到暂存区后的状态

场景1：当你改乱了工作区某个文件的内容，想直接丢弃工作区的修改时，用命令git checkout -- file。

场景2：当你不但改乱了工作区某个文件的内容，还添加到了暂存区时，想丢弃修改，分两步，第一步用命令git reset HEAD <file>，就回到了场景1，第二步按场景1操作。

场景3：已经提交了不合适的修改到版本库时，想要撤销本次提交，参考版本回退一节，不过前提是没有推送到远程库。

4. 删除文件
git rm readme.txt
or
git add readme.txt



-------远程仓库-------
-------分支管理-------

aaaaaa>?