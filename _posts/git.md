$ git config --global user.name "yanghongkai"
$ git config --global user.email "email@example.com"

git clone https://github.com/yanghongkai/pytorch_study.git  # 从远程库clone

git remote  # 查看当前配置有哪些远程仓库

git remote -v #  -v --verbose 显示对应的clone地址

# fetch 只是将远端的数据拉到本地仓库，并不自动合并到当前工作分支，只有当你确实准备好了，才能手工合并
git fetch [remote-name]  # 从远程仓库抓取数据到本地

# git pull 命令自动抓取数据下来，然后将远端分支自动合并到本地仓库中当前分支。





# 创建空的仓库(git repository)
$ git init
# 添加文件到Git仓库，分两步：
$ git add <file> # 注意可反复多次使用，添加多个文件
$ git commit -m "introduction" # -m 后面输入的是本次的提交说明

$ git status     # 随时掌握工作去的状态
$ git differ     # git status 告诉你有文件被修改过，用git diff 可以查看修改内容。

# 添加远程仓库
git remote add [shortname] [url]
git remote add origin https://github.com/yanghongkai/pytorch_study.git

# 推送数据到远程仓库

git push [remote-name] [branch-name]

git push origin master # 把本地的master分支推送到origin服务器上（克隆操作会自动使用默认的master和origin名字）




查看分支：git branch
创建分支：git branch <name>
切换分支：git checkout <name>
创建+切换分支：git checkout -b <name>
合并某分支到当前分支：git merge <name>
删除分支：git branch -d <name>
$ git merge <branch>        #合并指定分支到当前分支
$ git rebase <branch>       #衍合指定分支到当前分支

git checkout -b dev
# 创建dev分支，-b 参数表示创建并切换，相当于以下两条命令：
git branch dev
git checkout dev

关联远程仓库
$ git remote add origin https://github.com/yanghongkai/tfcloud.git     # 关联一个远程库
$ git push -u origin master     # 关联后， 使用命令，第一次推送master分支的所有内容
$ git push origin master     #  此后，每次本地提交后，只要有必要，就可以使用命令，推送最新更改

$ git remote -v                   #查看远程版本库信息
$ git remote show <remote>        #查看指定远程版本库信息
$ git remote add <remote> <url>   #添加远程版本库
$ git fetch <remote>              #从远程库获取代码
$ git pull <remote> <branch>      #下载代码及快速合并
$ git push <remote> <branch>      #上传代码及快速合并
$ git push <remote> :<branch/tag-name>  #删除远程分支或标签
$ git push --tags                       #上传所有标签






