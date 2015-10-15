初学git

注1：本人系统为win 8.1

注2：[git官方教程](https://git-scm.com/book/en/)

+ 安装

 + 我的git for windows在git-scm.com下载，安装后显示三个程序，分别
是git cmd，git bash，和git gui。其中gui是人机交互界面（比较傻瓜），bash和cmd是命令输入界面。目前仍不清楚两个各自的作用。搜了一
下网络，我选择bash作为命令输入器。

 + 根据教程，也可以在github上下载git，安装以后应显示两个程序，分别是git gui和git shell。这个版本的git 仅适用win7后的系统。但我的
电脑win8.1仍安装失败，提示是连接相关网址出错。

+ 初始

 + 打开git bash

 + 设定用户名
        $ git config --global username "myname"

 + 设定邮箱
        $ git config --global user.email myname@mymail.com
 + 设定编辑器
        $ git config --global core.editor "'C:/Program Files/Notepad++/notepad++.exe' -multiInst -nosession"

   + git documentation上这么说：You may find, if you don’t setup an editor like this, you will likely get into a really confusing state when they are launched. Such example on a Windows system may include a prematurely terminated Git operation during a Git initiated edit.

 + 建立本地仓库
   + 因为已在github上建立了公共仓库，因此这里采用了直接复制github仓库的方式
            $ git clone https://github.com/myname/myrepo
   + 如果想在本机更改库名，则可以在命令后添加新名字
            $ git clone https://github.com/myname/myrepo newrepo


