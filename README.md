# CommitCodeToGitHub  
Using Git To Commit Your Code  

上传本地代码：  
1、在Github上创建Repository存储库  
2、为本地Code创建git仓库  
a.cmd->到自己代码的根目录  
b.创建git仓库：git init  
3、将项目的所有文件添加到git仓库中：git add .  
在此添加用户名密码：  
git config --global user.email "you@example.com"
git config --global user.name "Your Name"
4、提交到git仓库：git commit -m "提交时的注释语句"
5、将本地的仓库关联到Github：git remote add origin https://github.com/ThelemeGrand/CommitCodeToGitHub.git
注意：origin：远程库名称；GitHub库路径改为自己的
6、上传GitHub之前需要先pull：git pull origin master
注意如果报错信息为：fatal: refusing to merge unrelated histories
需要合并两个独立启动仓库的历史：git pull origin master --allow-unrelated-history
7、上传代码：git push -u origin master
中间可能会让你输入Username和Password，你只要输入github的账号和密码就行了
如果报错：
 ! [rejected]        master -> master (fetch first)
error: failed to push some refs to 'https://github.com/ThelemeGrand/WebAPI.git'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
使用：git push -f kzywebapi master（强制推送）

更新代码：
1、查看当前git仓库状态：git status
2、更新全部：git add *
3、体检更新并更新说明：git commit -m "更新说明"
4、先pull：git pull
5、push：git push origin master
