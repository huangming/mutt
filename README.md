Including files
=============

     README			    # this file
    .mutt/dot_muttrc    # .muttrc, link this to ~/.muttrc
    .mutt/aliases		# there's a sample for building your alias
    .mutt/bindings.rc	# config key bindings
    .mutt/colors.rc		# color config
    .mutt/mailcap		# I get this copy from the sample file
    .mutt/postponed		# Use to store the delay mail
    .mutt/priv.rc       # dirs and non-public stuff, (hooks, alternates, ...),you can change it to youself
    .msmtprc            # msmtp config(发件配置文件)  
    .procmailrc         # procmail config(过滤规则)
    .getmail/getmail    # 收信脚本
    .getmail/config/getmail.163     # 收信邮箱配置文件
    .getmail/log        # 收信日志
     Mail/*             # 信箱文件
About
=====

解决方案：msmtp发信，getmail4收信，procmail过滤， wvHtml w3m  处理word/html邮件内容

配置由 http://suchang.net/slack/Mutt.html 提供的配置改编而成。感谢原创作者。

更改的部分有：

1. 部分含路径的设置由muttrc迁移到priv.rc方便统一配置
2. 编码设置
3. 收信软件fectmail改为getmail4，更改缘由：http://pyropus.ca/software/getmail/faq.html#faq-about-why
4. 发件软件esmtp改为msmtp，更改缘由：http://zoomquiet.org/res/scrapbook/ZqFLOSS/data/20110506155957/
5. 处理邮件html内容的软件由lynx改为w3m,更改缘由：http://forum.ubuntu.org.cn/viewtopic.php?t=201736
6. 增加部分快捷键设定（处于注释状态）
7. 信箱所需文件夹已经新建好

Usage
======

git安装:

    $ sudo apt-get install mutt msmtp getmail4 procmail wvHtml w3m 
    $ git clone git://github.com/huangming/mutt.git
    $ mv mutt/* ~/
    $ rm mutt
    $ ln -s ~/.mutt/dot_muttrc ~/.muttrc
    
或者下载压缩包[mutt.tar.gz](https://nodeload.github.com/huangming/mutt/tarball/master)进入包所在目录安装：

    $ sudo apt-get install mutt msmtp getmail4 procmail wvHtml w3m 
    $ tar -xzvf mutt.tar.gz
    $ mv mutt/* ~/
    $ rm mutt
    $ ln -s ~/.mutt/dot_muttrc ~/.muttrc

安装完成后用编辑器打开 `~/.msmtprc` `~/procmailrc` `~/.getmail/config/getmailrc.163` `~/.getmail/config/getmailrc.gmail`
把里面的邮箱地址、用户名、密码改为你自己的。

Notes
=====

priv.rc里面的配置（主要是路径和信箱名称）可以根据自己需要更改。多用户收件是通过在`~/.getmail/config/`建立多个配置文件来处理的。每个文件对应一个邮箱，例如你想增加一个QQ的收件账户，只需在`~/.getmail/config/`建立一个`getmailrc.qq`的文件，编辑内容格式仿照我给的163的例子即可。而多用户发件是在`~/.msmtprc`一个文件中配置的。
