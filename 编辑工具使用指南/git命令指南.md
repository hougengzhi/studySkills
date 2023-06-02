# git 拉取分支代码

  比如我的仓库地址是git@git.labs.zhonghao.com:services/xxx.git，分支是hzh-v1
  则拉取该分支下代码的方式就是：

  git clone -b hzh-v1 git@git.labs.zhonghao.com:services/xxx.git

# git 提交代码命令

  git pull 先拉取代码
  git status  查看文件状态
  git add  文件名
  git commit -m “修改项目代码”
  git push

# git 删除文件
  
  git rm -r --cached a/2.txt //删除a文件夹下的2.txt文件   
  git rm -r --cached a //删除a文件夹
  git commit -m "删除a目录下的2.txt文件" 
  git push

# git 恢复删除文件

  git status命令查看本地文件和远程文件的差异 
  git reset HEAD [被删文件夹名称] 这个命令将文件放在暂存区
  git checkout [被删文件夹名称] 这个命令将暂存区文件拉回本地

# git 查看分支

  git branch -a

# git 合并分支

  git merge  "分支路径"

# git 切换分支

  git checkout -b  "分支路径"

# git合并本地分支并推动到远程服务器
  
  git branch -a   查看分支
  git checkout "分支名"
  git merge "分支名"
  提交到远程分支

# git 远程服务版本回退

  - 本地分支版本回退的方法
     
    如果在本地做了错误提交，回退版本的方法为：
    
    - 使用git reflog命令查看历史提交记录的commit id
    - 使用git reset --hard commit_id，commit_id为你要回退版本的commit id的前几位

  - 自己的远程分支版本回退的方法
    
    - 使用git reflog命令查看历史提交记录的commit id
    - 使用git reset --hard commit_id回退本地分支，commit_id为你要回退版本的commit id的前几位
    - 使用git push -f强制推送到远程分支

# git 查看当前账号名及修改

  - 查看当前登录账号
    
    git config user.name

  - 查看当前登录邮箱
    
    git config user.email

  - 修改用户名和邮箱:
  
    git config --global  user.name  "Your_username"
    git config  --global  user.email  "Your_email"
    

# [如何在github上创建公共密钥](https://blog.csdn.net/qq_29820687/article/details/119521481) 
  1. 如何在github上创建公共密钥
  2. 输入 cd~/.ssh，并回车
  3. 再输入ssh-keygen -t rsa -C “xxxxx@gmail.com”

      特别注意后面是跟自己邮箱
  4. 多按几次Enter回车就会出现  公钥 私钥
  5. 这时候我们只需要找到以下目录的双击打开下面的公钥，将公钥的内容添加到github上就可以了  

  