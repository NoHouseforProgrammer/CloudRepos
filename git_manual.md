# git manual

## 一、基本操作

git init
: 	初始化仓库

git clone [url]
:   拷贝一份远程仓库，也就是下载一个项目

git add 
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

git commit	
:   提交暂存区到本地仓库

git reset	
:   回退版本

git rm	
:   删除工作区文件

git mv	
:   移动或重命名工作区文件

git log	
:   查看历史提交记录

git blame [file]
:   以列表形式查看指定文件的历史修改记录

git remote
:   远程仓库操作

git fetch
:   从远程获取代码库

git pull
:	下载远程代码并合并

git push
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

