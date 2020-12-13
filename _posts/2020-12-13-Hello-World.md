---
layout: post
title: Hello World & Some basic Github operations
---

1. git clone
远程操作的第一步，通常是从远程主机克隆一个版本库，这时就要用到git clone命令。

```sh
$ git clone <版本库的网址>
```
2. git remote
为了便于管理，Git要求每个远程主机都必须指定一个主机名。git remote命令就用于管理主机名。

不带选项的时候，git remote命令列出所有远程主机。

3. git fetch
一旦远程主机的版本库有了更新（Git术语叫做commit），需要将这些更新取回本地，这时就要用到git fetch命令。

```sh
$ git fetch <远程主机名>
```

4. git pull
git pull命令的作用是，取回远程主机某个分支的更新，再与本地的指定分支合并。它的完整格式稍稍有点复杂。


$ git pull <远程主机名> <远程分支名>:<本地分支名>

5. git push
git push命令用于将本地分支的更新，推送到远程主机。它的格式与git pull命令相仿。

```sh
$ git push <远程主机名> <本地分支名>:<远程分支名>
```
注意，分支推送顺序的写法是<来源地>:<目的地>，所以git pull是<远程分支>:<本地分支>，而git push是<本地分支>:<远程分支>。

如果省略远程分支名，则表示将本地分支推送与之存在"追踪关系"的远程分支（通常两者同名），如果该远程分支不存在，则会被新建。

```sh
$ git push origin master
```
上面命令表示，将本地的master分支推送到origin主机的master分支。如果后者不存在，则会被新建。

