# Note 关于学习git和github
> 该note的所有内容都是基于[廖雪峰的教程](https://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000/0013743256916071d599b3aed534aaab22a0db6c4e07fd0000)

## 下载安装git
以ubuntu为例，`sudo apt-get install git`
## 创建新的版本库(repository)
```bash
mkdir /home/xyw/physics/book/practice/git
cd git
```
通过git init 命令将这个目录变成git可以管理的仓库：
```bash 
git init
```
这样就创建了一个空白的库，并在自动在目录下添加了.git目录，这个目录是用来管理git用的，不要动！！！！

## 将文件添加到文件库

> git只能将你每次改动的信息保存记录下来

```git
git add [文件名]
git commit -m "[提交的说明]"
```

第一行为添加文件给git仓库
第二行为将文件提交给仓库，其中`-m`表示的本次提交的说明

然后修改文件后，键入
`git status`　表示查看仓库当前的状态
`git diff` 查看文件修改的地方difference

但是现在文件需要重新add
```git
git add [文件名]
```
若此时键入　`git status` 将会显示文件已修改，然后可以放心的提交了　`git commit -m "[提交的说明]`
通过不停的修改，就会不停的提交修改到版本库里。git每一个修改后的文件成为commit，一旦文件改乱了或者删了，可以从最近的一个commit恢复，就像一个游戏存档一样。
