
## 1.An introduce to shell 
### Pre-concept 虚拟机
    虚拟机是模拟计算机的计算机程序
### 如今使用虚拟机的原因
    隔离程序员和项目：日常环境和项目环境保持独立，互不干扰
    模拟软件的部署环境：在Window和Mac OS环境的系统中运行linux代码
### VirtualBox&Vagrant
      1.相似之处是Vagrant和Docker都是虚拟化技术。
      2.Vagrant是基于Virtualbox的虚拟机来构建开发环境，而Docker则是基于LXC(LXC)轻量级容器虚拟技术。  
      3.Vagrant就是你的开发环境的部署工具；而docker是你的运行环境部署工具。
      为什么开发环境需要单独一个部署工具？
      a.开饭环境的快速部署（未部署的机器）
      b.开发环境的快更迭（已部署的机器）
     Vagrant本质：说白了vagrant就是一个普普通通的装了一个Linux的VirtualBox虚拟机，
                 配以vagrant 团队为之开发的一系列套件，辅助完成诸如安装初始化、文件同步、ssh、部署环境升级、
                 功能插件安装等等一些列问题的开发环境部署套件。也没什么好神秘的。
    总的来说：
    vagrant更适合给开发大爷们创造一个统一的开发、测试、接近于完全隔离的环境，以及提高对高配机的闲置利用。
    docker更方便地解决了同一机器上的环境隔离，以及提高运维锅们解决部署时环境依赖的效率。



[VAGRANT 和 Docker的使用场景和区别?-----大杰哥](https://www.zhihu.com/question/32324376/answer/123239426)  
[VAGRANT 和 Docker的使用场景和区别?-----cikenerd](https://www.zhihu.com/question/32324376/answer/91562849)


   [Download VirtualBox](https://www.virtualbox.org/wiki/Downloads)
   [Download Vagrant](https://www.vagrantup.com/downloads.html)
   

下载一份配置文件
在git bash运行以下命令
```
cd D:\\ShellScript\\shell
vagrant up

```
报错：
```
The version of powershell currently installed on this host is less than
the required minimum version. Please upgrade the installed version of
powershell to the minimum required version and run the command again.
```
解决方法：
[How to upgrade PowerShell version from 2.0 to 3.0](https://stackoverflow.com/questions/19902239/how-to-upgrade-powershell-version-from-2-0-to-3-0?utm_medium=organic&utm_source=google_rich_qa&utm_campaign=google_rich_qa)
```
vagrant ssh
```

### 基本命令
    1.^c查看说明，在奇怪的状态下可用
    2.exit  ctr+D
    3.ls 查看当前目录下的文件和目录
    4.curl http://udacity.github.io/ud595-shell/stuff.zip -o things.zip
    5.sudo apt-get install cowsay (Ubuntu和Debian)
    6.sudo yum install cowsay(Redhat和CentOS用户)
    date| hostname  | host | url |expr 2+2 | bash --version| uname | history

### Shell command VS python fuc
    1.run program | organize program
    2.code,name,take args

### git bash & git cmd

## 2.Shell commands
    1.Crt+R:检索历史命令
    2.unzip:解压文件
    3.cat :打印出文件（concatenate）拼接文件
    4.tab快速填充 已显示的内容
    5.diff 比较文件的不同
    6.man to display the manual
    7.ls不会列出.开头的文件（这些文件用于缓存或者配置文件等不需要关注的部分）
    8.ls -l
    9.ls -a:all files inclu
    10.sort  a c b +CRT+D
    11.bc
    12.less:内置搜索+正则匹配功能的浏览
    13.nano：编辑

## 3.File System
###  The File System Tree
    1.文件名可以为任意的除了/的字符：命名可用两种方式表示：
        a.引用：'file name!'
        b.转义：file\ name\!
    2.文件（系统）树：所有的文件以树的形式组织，所以必须通过根路径去延伸
        a.用/表示根目录
        b.pwd打印工作目录
        c.cd 跳转目录 
        d.cd.. 前往上一级目录
    3.绝对路径和相对路径
        a.绝对路径：从跟路径开始逐级检索
        b.相对路径：与当前目录的相对路径。../表示上级目录、./当前目录
        c.cd  返回根目录
    4.文件操作
     mv :移动和重命名
     cp:复制文件 
     mkdir path/dirname  
    5.通配符查找
     glob():searches for all  the  pathnames  matching  pattern
     ls *{css,html)
     ls bea?.pgn be??.pgn(匹配任意单个字符)
