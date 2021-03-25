1、首次提交代码：

git init    ------>      git 初始化

git add .   ------>   添加所有需要提交的git文件

git status   ------>    查看当前文件夹git 的状态（可操作可不操作这一步）

git remote add origin url   添加远程仓库服务器地址 （url服务器地址）

git remote -v  查看该文件夹远程的地址（可操作可不操作）

git commit -m '需要描述做了什么改动的内容'           提交代码到缓冲区
x
git push -u origin master     提交代码（第一次提交最好用git push -u origin master， 后来提交就用git push origin master即可）

git pull --rebase origin master  （假设该文件夹提交不上去报错 failed to push some refs to 'https://gitee.com/liuhanhanya/time-of-attack.git'）   时，意味着当前文件夹和远程文件夹内容不一致，执行这行命令的意思是拉取远程代码使他们保持一致即可





2、非首次提交代码

git  add -A  提交修改文件的命令（ -A为你修改的全部文件 ）

git commit -m '描述'              提交代码到缓冲区

git push origin master           提交代码

这是常用的提交代码到远程仓库的命令，一般就是这些



3.   git 解决代码提交冲突
在提交分支的时候 提前 git pull origin 分支名字   --rebase
出现冲突  然后小乌龟解决冲突   
git add .
git rebase --continue
然后 esc加上 shift 加  ：（ 冒号的意思 ）wq 返回      然后 git push origin 分支名字  提交成功


4. git 强制远程代码覆盖本地代码的操作

git fetch --all
git reset --hard origin/分支名字
git pull


5. git 版本的回退操作

git log   打印提交日志   （ 推出日志的需要点击 "q" 按键  ）

git reset --hard ( 后面加上 日志commit 的字符串即可 )


6.git 想保存当前代码 有不想提交的命令

git stash save ( 加上备注 )

git stash list  备注（ 这是把保存的列表答打印出来 ）

git rebase pop  备注( 全部弹出 )

git rebase ( 加上列表的返回值 )


7. git 删除远程仓库地址

git remote -rm origin ( 删除地址 )

git branch -d 备注 ( 删除分支名字 )

git branch -r 备注（ 查看远程分支 ）

git branch -a 备注 （ 查看全部分支 包括本地和远程仓库的 ） 

8. git 分支的合并 和 分支的切换
   
   git merge "分支名字"

   git merge --abort 会退

   git checkout "分支名字"

   git branch "添加分支"

  git push origin 分支名/分支名 （把代码复制到分支上面）
 




