# 课程设计日记
## 在LINUX下ubuntu安装MySQL

1.用vim打开源列表文件。
```
sudo vim /etc/apt/sources.list
```

2.将下面的源粘贴到源列表里。

```
deb http://mirrors.aliyun.com/ubuntu/ xenial main restricted universe multiverse
deb http://mirrors.aliyun.com/ubuntu/ xenial-security main restricted universe multiverse
deb http://mirrors.aliyun.com/ubuntu/ xenial-updates main restricted universe multiverse
deb http://mirrors.aliyun.com/ubuntu/ xenial-backports main restricted universe multiverse
##测试版源
deb http://mirrors.aliyun.com/ubuntu/ xenial-proposed main restricted universe multiverse
# 源码
deb-src http://mirrors.aliyun.com/ubuntu/ xenial main restricted universe multiverse
deb-src http://mirrors.aliyun.com/ubuntu/ xenial-security main restricted universe multiverse
deb-src http://mirrors.aliyun.com/ubuntu/ xenial-updates main restricted universe multiverse
deb-src http://mirrors.aliyun.com/ubuntu/ xenial-backports main restricted universe multiverse
##测试版源
deb-src http://mirrors.aliyun.com/ubuntu/ xenial-proposed main restricted universe multiverse
# Canonical 合作伙伴和附加
deb http://archive.canonical.com/ubuntu/ xenial partner
deb http://extras.ubuntu.com/ubuntu/ xenial main
```

3.更新源
```
sudo apt-get update
```


4.执行下面命令：
```
sudo apt-get install tasksel
```
      安装Apache和MySQL。

5.安装LAMP环境:
      输入命令 sudo tasksel install lamp-server , 即可完成LAMP的安装。
通过命令 sudo tasksel 可查看LAMP安装是否成功。需要指出的是，通过tasksel软件包不仅可以安装LAMP组件，还可以安装其他服务器组件，比如DNS服务器，Mail服务器，打印服务器等。



6.连接Mysql
```
键入命令mysql -u root -p，回车后提示你输密码.输入密码后进入MySQL中，MySQL的提示符是： mysql>
```


7.退出MySQL
```
mysql>exit
```


## git的基本使用



1.ubuntu Linux 安装git
```
sudo apt-get install git
```


2.创建版本库
* 首先创建一个目录用来存放库
```
$ mkdir html
$ cd html
```
* 在使用git init命令将目录创建成git仓库
```
$ git init
Initialized empty Git repository in /home/user/html/.git/
```

3.增加文件并编辑文件
```
$ touch README
$ vim README
$ git status
$ git add README
$ git status
```


4.提交
```
gir commit
```



5.配置用户信息

* 配置用户信息
```
$ git config --global user.name
```

* 配置用户邮箱
```
$ git config --global user.email
```

* 配置编辑提交的编译器
```
$ git config --global core.editor vim
```

6.查看提交的信息
```
$ git log
```


## Linux的基本使用


1.基本的文件操作

* 文件的创建、删除、复制、重命名、移动
* 列出文件列表
* 查看文件内容

```
touch  file
cp file file1
cp file  /home/linux/file1
mv file   file2
mv file  /home/linux/
ls -al  .
cat  file
```

2.基本的目录操作

* 目录的创建、删除、复制、重命名、移动
* 列出目录列表
* 目录中查找文件


```
mkdir dir
cp dir   dir1  -a
cp dir   /home/linux/dir2  -a
mv dir  dir2
mv dir  /home/linux/
rm  dir  -rf
ls -d  dir
find  ./dir  -name  "filename"
```

3.文件的归档和压缩

* 使用gzip和gunzip对文件进行压缩和解压缩
* 使用bzip2和bunzip2对文件进行压缩和解压缩
* 使用tar对文件和目录进行压缩和解压缩

```
gzip  filename
bzip2  filename
gunzip filename
bunzip2  filename
tar czvf  file.tar.gz dir
tar cjvf  file.tar.bz2 dir
tar cJvf  file.tar.xz  dir
tar xvf  file.tar.gz
tar xvf  file.tar.xz
```
4.Vim的基本使用

```
i：在当前字符的左边插入
I：在当前行首插入
a：在当前字符的右边插入
A：在当前行尾插入
o：在当前行下面插入一个新行
O：在当前行上面插入一个新
h: 向前移动一个字符
j: 向上移动一行
k: 向下移动一行
l: 向后移动一个字符
yy: 复制当前一行
dd:剪切当前一行
p: 粘贴内容到游标之后
P: 粘贴内容到游标之前
```

