git rm --cached <filename>   移除通过 add . 添加的文件



pull 命令就是 fetch 和 merge 命令的组合





删除远程分支： git push --delete origin devel

重命名远程分支：在git中重命名远程分支，其实就是先删除远程分支，然后重命名本地分支，再重新提交一个远程分支。

重命名本地分支：git branch -m devel develop

推送本地分支：git push origin develop



在分支master上生成一个标签：git tag -a v0.1.0 master

把本地tag推送到远程     git push --tags

获取远程tag       git fetch origin tag <tagname>

切换到标签        git checkout [tagname]

查看标签的版本信息：   git show v0.1.2

删除标签
         误打或需要修改标签时，需要先将标签删除，再打新标签。
         git tag -d v0.1.2


git push origin v0.1.2 # 将v0.1.2标签提交到git服务器
git push origin --tags # 将本地所有标签一次性提交到git服务器







查看远程分支    git branch -a

删除远程分支和tag     git push origin --delete <branchName>
                      git push origin --delete tag <tagname>

查看b1的状态：        git remote show origin


fetch之后删除掉没有与远程分支对应的本地分支：   git fetch -p





查看分支：git branch

创建分支：git branch <name>

切换分支：git checkout <name>

创建+切换分支：git checkout -b <name>

合并某分支到当前分支：git merge <name>

删除分支：git branch -d <name>





日志输出：  git log --pretty=oneline


多人协作的工作模式通常是这样：

首先，可以试图用git push origin branch-name推送自己的修改；

如果推送失败，则因为远程分支比你的本地更新，需要先用git pull试图合并；

如果合并有冲突，则解决冲突，并在本地提交；

没有冲突或者解决掉冲突后，再用git push origin branch-name推送就能成功！

如果git pull提示“no tracking information”，则说明本地分支和远程分支的链接关系没有创建，用命令git branch --set-upstream

branch-name origin/branch-name



查看远程库信息，使用git remote -v；

本地新建的分支如果不推送到远程，对其他人就是不可见的；

从本地推送分支，使用git push origin branch-name，如果推送失败，先用git pull抓取远程的新提交；

在本地创建和远程分支对应的分支，使用git checkout -b branch-name origin/branch-name，本地和远程分支的名称最好一致；

建立本地分支和远程分支的关联，使用git branch --set-upstream branch-name origin/branch-name；

从远程抓取分支，使用git pull，如果有冲突，要先处理冲突。






场景1：当你改乱了工作区某个文件的内容，想直接丢弃工作区的修改时，用命令git checkout -- file。

场景2：当你不但改乱了工作区某个文件的内容，还添加到了暂存区时，想丢弃修改，分两步，第一步用命令git reset HEAD file，就回

到了场景1，第二步按场景1操作。

场景3：已经提交了不合适的修改到版本库时，想要撤销本次提交，参考版本回退一节，不过前提是没有推送到远程库。


版本回退
         Git必须知道当前版本是哪个版本，在Git中，用HEAD表示当前版本，也就是最新的提交3628164...882e1e0（注意我的提交ID和

你的肯定不一样），上一个版本就是HEAD^，上上一个版本就是HEAD^^，当然往上100个版本写100个^比较容易数不过来，所以写成

HEAD~100。

HEAD指向的版本就是当前版本，因此，Git允许我们在版本的历史之间穿梭，使用命令git reset --hard commit_id。

穿梭前，用git log可以查看提交历史，以便确定要回退到哪个版本。

要重返未来，用git reflog查看命令历史，以便确定要回到未来的哪个版本。










start a working area:

clone     clone a repository into a new directory

init      create an empty git repository or reinitialize an existing one



work on the current change:

add   add file coontents to the index

mv    move or rename a file, a directory,  or a symlink

reset   reset curretn HEAD  to  the specified  state

rm     remove filees from the working tree and from the index



examine  the history  and  state

bisect    use binary search to find the commit that introduced a bug

grep      print lines matching a pattern

log   show commit logs

show   show various types  of objects

status     show the working tree status



grow, mark  and tweak your common history

branch    list, create, or delete branches

checkout    switch branches or restore working tree files

commit      record   changes   to the repository

diff      show  changes  between commits, commit and working tree, etc

merge     join two or more development histories together

rebase    reapply commits  on top of another base tip

tag     create, list, delete or verify a tag object singed  width gpg


collaborate:

fetch     download objects and refs form another repository

pull   retch from and intergrate  with another repository or a local branch

push    update remote refs along with associated objects





git文档：http://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000



===============================================================================================

 Sublime   Text
===============================================================================================



DocBlockr                  生成文档注释
Browser Refresh            自动刷新浏览器
Material Theme             主题
HTML/CSS/JS Prettify       保存时是否自动格式化  快捷键：ctrl+shift+h
AutoPrefixer               自动添加css前缀
Better Completion          js css  html 自动提示
SublimeTextTrans           界面透明




Git操作        Ctrl+Shifp+p ==》 git:

菜单栏隐藏   Ctrl+Shifp+p ==》 view:


查找想要的文件  Ctrl + p

快速查找文件中方法    Ctrl + r

Ctrl + d     选中光标所占的文本，继续重复操作则会选中相同的文本

Ctrl + click  添加多个光标

Ctrl + Alt + up/down   向上添加多行光标

shift + up/down     向上选中多行


Snippets（代码片段）    输入一个定义了代码片段的文本， 然后按tab键。

css前缀  ctrl + b

