git的使用步骤：

1.全局配置用户名和邮箱（仅初次安装需要）
$ git config --global user.name "K2844"
$ git config --global user.email "349053795@qq.com"

2.选择要初始化的本地仓库（告诉git哪个仓库需要管理，可直接在要选择的文件进入然后初始化）
 $ git init（必须）

3可查看状态，获得步骤提示
$ git status

4.添加文件到缓存区中
$ git add readme.txt（单个文件）
$ git add 文件名 文件名 文件名    （多个文件）
$ git add .                    (添加当前目录到缓存区中)

5.提交至版本库（可重复使用add和commit）
$ git commit -m "注释内容" （$ git commit -m "新建文件readme"）

6.查看版本（ (HEAD -> master)是最新的更新版本）
$ git log
$ git log --pretty=oneline（在一行显示一条记录）

7.版本回退（hard后面跟着回退后的版本号）
$ git reset --hard 4a1de3aba1c00a3f9096e830bcd56d56a118a5e7

8.回退后，又想回到回退前的最新版本（版本号短了些，但也能用，4位数就够）
$ git reflog 查看历史记录，得到最新的commit id
$ git reset --hard 3c5a859

9.克隆github项目到本地	（选择一个文件夹,克隆的自带.git,不用再初始化）
$ git clone "url地址"
$ git add 添加到缓存区的文件
$ git commit -m"备注信息"提交到本地仓库

10.提交到线上仓库
$ git push 提交到线上仓库

11.拉取线上仓库	（GitHub仓库的更新项目到本地仓库）
$ git pull

12.查看分支	（当前分支前面会有小棉花图标）
$ git branch

13.创建分支
$ git branch 分支名

14.切换分支
$ git checkout 分支名

15.合并分支
$ git add .           		添加到缓存区的文件
$ git commit -m"备注信息"	提交到本地仓库
$ git checkout master 	切换到主分支
$ git merge 分支名  	合并分支

16.删除分支（合并后分支可以删掉 注：先退出要删除的分支，以免不能删除）
$ git branch -d 分支名