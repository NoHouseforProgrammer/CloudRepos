# git manual

## 一、基本操作

git init
: 	初始化仓库

git clone [url]
:   拷贝一份远程仓库，也就是下载一个项目

git add 
:   添加文件到暂存区
    -   git add [file1] [file2]
        :   添加一个或多个文件到暂存区
    -   git add [dir]
        :   添加指定目录到暂存区，包括子目录
    -   git add .
        :   添加当前目录下的所有文件到暂存区

git status
:   查看仓库当前的状态，显示有变更的文件

git diff	
:   比较文件的不同，即暂存区和工作区的差异
    - git diff
        :   尚未缓存的改动
    - git diff --cached
        :   查看已缓存的改动
    - git diff HEAD
        :   查看已缓存的与未缓存的所有改动
    - git diff --stat
        :   显示摘要而非整个 diff

git commit	
:   提交暂存区到本地仓库
    - git commit -m [message]
        :   [message] 可以是一些备注信息。
    - git commit [file1] [file2] ... -m [message]
        :   提交暂存区的指定文件到仓库区
    - git commit -a
        :   -a 参数设置修改文件后不需要执行 git add 命令，直接来提交

git reset [--soft | --mixed | --hard] [HEAD]
:   回退版本
    - --mixed 为默认，可以不用带该参数，用于重置暂存区的文件与上一次的提交(commit)保持一致，工作区文件内容保持不变
    - --soft 参数用于回退到某个版本
    - --hard 参数撤销工作区中所有未提交的修改内容，将暂存区与工作区都回到上一次版本，并删除之前的所有信息提交
    - git reset HEAD 
        命令用于取消已缓存的内容
        
        + HEAD 表示当前版本

        + HEAD^ 上一个版本

        + HEAD^^ 上上一个版本

        + HEAD^^^ 上上上一个版本

        + 以此类推...

        可以使用 ～数字表示
        + HEAD~0 表示当前版本

        + HEAD~1 上一个版本

        + HEAD^2 上上一个版本

        + HEAD^3 上上上一个版本

        + 以此类推...

git rm	[-f] [--cached] [file]
:   删除工作区和暂存区文件
    - -f 强制删除
    - --cached 只删除暂存区

git mv	[-f] [file] [newfile]
:   移动或重命名工作区文件

git log	
:   查看历史提交记录
    - online 查看简洁版本
    - --graph 查看历史中什么时候出现了分支、合并
    - --reverse 参数来逆向显示所有日志
    - --author=[user] 

git blame [file]
:   以列表形式查看指定文件的历史修改记录

git remote
:   远程仓库操作
    - git remote -v 
        :   显示所有远程仓库
    - git remote show [url] 
        :   显示某个远程仓库的信息
    - git remote add [shortname] [url] 
        :   添加远程版本库   
    - git remote rm name  
        :   删除远程仓库   
    - git remote rename old_name new_name 
        :   修改仓库名

git fetch
:   从远程获取代码库

git pull [远程主机名] [远程分支名:本地分支名]
:	下载远程代码并合并

git push [远程主机名] [远程分支名:本地分支名]
:	上传远程代码并合并

## 二、分支管理
git branch 
-   git branch
    :   列出分支
-   git branch [branchname]
    :   创建分支命令

git checkout [branchname]
:   切换分支

git branch -d [branchname]
:   删除分支

