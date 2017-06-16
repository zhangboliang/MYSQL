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




