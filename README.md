# shop
本地提交github项目
1.在本地建一个空的文件夹
git init //初始化为可管理的git仓库
2.可以查看当前状态(红色)提示项目粘贴过来了，但是还没有到git仓库上
git status //查看当前项目状态
3.把项目粘贴到本地的git仓库里面
git  add . //项目添加到仓库（注意：空格隔开）
4.查看当前状态(当前状态为绿色)
git status //查看当前项目状态
5.提交项目到仓库中
git commit -m 'first commit' //-m后面引号里面是本次提交的注释内容,最好写上，不然会报错
6.本地git仓库和github仓库之间的传输是通过ssh加密的，所以连接时需要设置一下
7.创建SSH KEY,查看C盘用户目录下有没有.SSH目录，有的话看下里面有没有id_rsa和id_rsa.pub这个文件，
有就跳到下一步，没有就通过下面命令创建
ssh-keygen -t rsa -C 'yourmail@qq.com' //你的邮箱
一路回车,在c盘.ssh目录下找到id_rsa和id_rsa.pub这两个文件
8.登录github,找到右上角的图标，打开点进里面的Settings，再选中里面的SSH and GPG KEYS，点击右上角的New SSH key，
然后Title里面随便填，再把刚才id_rsa.pub里面的内容复制到Title下面的Key内容框里面，最后点击Add SSH key，这样就完成了SSH Key的加密。
9.在Github上创建一个Git仓库。
10.在github上创建好之后我们就可以和本地仓库进行关联了，根据建好的git仓库页面的提示，可以在本地仓库的命令输入：
git remote add origin https://github.com/guyibang/TEST2.git //注意：origin后面加的是你的github上建好的仓库地址
11.关联好之后我们就可以把本地仓库的所有内容推送到远程仓库上(也就是github)上了
git push -u origin master
由于新建的远程仓库是空的，所以要加上-u这个参数，等远程仓库有了内容之后，下次再从本地上传内容的时候，只需下面这样就好了 
git push origin mastr
12.刷新github上的页面进入刚才新建的那个仓库里面就发现项目已经上传成功了




