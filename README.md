<h1 id="intro">Command For GitHub</h1>

git rm --cached `<filename>`   移除通过 add . 添加的文件


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

删除远程分支和tag     git push origin --delete `<branchName>`
                      git push origin --delete tag `<tagname>`

查看b1的状态：        git remote show origin


fetch之后删除掉没有与远程分支对应的本地分支：   git fetch -p





查看分支：git branch

创建分支：git branch `<name>`

切换分支：git checkout `<name>`

创建+切换分支：git checkout -b `<name>`

合并某分支到当前分支：git merge `<name>`

删除分支：git branch -d `<name>`







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
