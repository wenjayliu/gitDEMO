### Linux 或 git 常用命令
`git`：Linus花了两周时间自己用C写了一个分布式版本控制系统。  
[Git for Windows](https://git-scm.com/download/win) 客户端 `git bash`提供了一个类似于linux的终端，可以使用linux的大部分常用命令。
命令的处理程序实际上在git安装目录下的usr/bin目录下。  

#### linux 命令  
- 文件目录  
```
$ ls      // 显示文件或目录 可选参数 -l  -a
$ mkdir   // 创建目录
$ touch   // 创建空文件
$ cat     // 查看文件内容
```
- vim 编辑  
vim三种模式：命令模式、插入模式、编辑模式。使用ESC或i或：来切换模式。
```
$ vi <filename>    // 打开或新建文件
ESC                // 命令模式
i                  // 编辑模式
:q                 // 退出
:q!                // 强制退出
:wq                // 保存并退出
```

#### git 命令
====


### 查看操作  
> git status                        // 查看状态
> 
> git log                           // 查看日志文件
> git log --pretty=oneline          // 查查简单日志 history
> git reflog                        // 查看查看命令历史
> 
> git diff                          // 查看文件修改（不包括增加的文件）
> 
> git branch                        // 查看分支


### 提交操作
img

> git add xyz                       // 添加xyz文件至index
> git add .                         // 增加当前子目录下所有更改过的文件至暂存区 index
> git commit -m 'xxx'               // 提交
> git commit --amend -m 'xxx'       // 合并上一次提交（用于反复修改）
> git commit -am 'xxx'              // 将add和commit合为一步

### 回滚操作  
回滚前先执行`查看`操作,注意 `revert` (撤销) 和 `reset`(回滚)。  
- git revert会生成一个新的commit，将之前的某个commit的修改恢复过来
- git reset会将HEAD移动到某个commit上，换种说法就是将某个commit变成最后一个commit

> git reset --hard HEAD^            // 回滚到上一个版本
> git reset --hard                  // 回滚到上一个版本
> git checkout -- <file>            // 放弃工作区修改
> git reset HEAD <file>             // 放弃缓存区提交

### 分支操作

> git branch <name>                  //创建分支
> 
> git checkout master                // 切换分支
> git merge dev                      // 合并某分支到当前分支
> 
> git merge --no-ff -m ":bookmark: 发布1.0.9版本" dev
> git log --graph --pretty=oneline --abbrev-commit




### 远程

> git remote add origin git@github.com:wenjayliu/gitDEMO.git

### 状态
[](https://www.liaoxuefeng.com/files/attachments/0013849077337835a877df2d26742b88dd7f56a6ace3ecf000/0)







### 参考资料
【[git 官方文档](https://git-scm.com/docs)】
【[廖雪峰 git 教程](https://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000)】


