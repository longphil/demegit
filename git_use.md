# git仓库使用 #
##  创建本地仓库  ##
- 安装git Bash 
- ip：https://git-for-windows.github.io/
- 命令：git version 查看版本号，检查是否安装成功
## 用户权限设置 ##
$ git config --global user.name "Your Name" (设置用户名)
$ git config --global user.email "email@example.com" （设置常用邮箱，最好与guihub用的邮箱一致）
## 初始化仓库 ##
命令：git init（目录不能包含中文）
目录下多了一个.git的目录，表是仓库创建成功
## 文件添加到本地仓库 ##
1. git add demo.txt 告诉git，把文件添加到仓库
2. git commit -m "add file" 提交文件到仓库，添加注释


- git status 查看是否有文件未提交
- git diff 查看修改内容
- 删除文件：1.rm demo.txt   2.git commit 
示例：
$ git add file1.txt
$ git add file2.txt file3.txt
$ git commit -m "add 3 files."

## 远程仓库 ##
1. 注册github账号，
2. 创建SSH Key（只要把每台电脑的Key都添加到GitHub）
ssh-keygen  -t rsa –C "youremail@example.com
在用户目录先生成.ssh文件夹,打开id.rsa.pub,复制key，回到github上，进入 Account Settings（账户配置），左边选择SSH Keys，Add SSH Key,title随便填，粘贴在你电脑上生成的key。
测试是否连接上github
ssh -T git@github.com
- 异常处理：ssh阻塞了22端口
- 处理方式：在.ssh文件夹下新增文件![](http://i.imgur.com/kyy8fDm.jpg)

## 新建远程库（在github创建一个Git仓库） ##
- 登录github上，然后在右上角找到“create a new repo”创建一个新的仓库
- 本地仓库关联github
$ git remote add origin https://github.com/tugenhua0707/testgit.git
或者
$ git remote add origin git@github.com:tugenhua0707/testgit.git

## 仓库同步到远程 ##
git push -u origin master(第一次)/git push origin master

## 从远程克隆到本地 ##
git clone https://github.com/longphil/demegit
