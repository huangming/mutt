
 Including files
=============

README			# this file
.mutt/dot_muttrc        # .muttrc, link this to ~/.muttrc
.mutt/aliases		# there's a sample for building your alias
.mutt/bindings.rc	# config key bindings
.mutt/colors.rc		# color config
.mutt/mailcap		# I get this copy from the sample file
.mutt/postponed		# Use to store the delay mail
.mutt/priv.rc       # dirs and non-public stuff, (hooks, alternates, ...),you can change it to youself

About
=====

msmtp发信，getmail4收信，procmail过滤， wvHtml w3m  处理word/html邮件内容
配置由http://suchang.net/slack/Mutt.html提供的配置改编而成。
更改的部分有：
# 部分含路径的设置由muttrc迁移到priv.rc方便统一配置
# 编码设置
# 收信软件fectmail变为getmail4
# 处理邮件html内容的软件由lynx改为w3m
# 增加部分快捷键设定（处于注释状态）
# 信箱文件夹已经新建好

Usage
======

git安装:

$ sudo apt-get install mutt msmtp getmail4 procmail wvHtml w3m 
$ git clone git://github.com/huangming/mutt.git ~/
$ ln -s ~/.mutt/dot_muttrc ~/.muttrc

或者下载压缩包mutt.tar.gz安装：

$ sudo apt-get install mutt msmtp getmail4 procmail wvHtml w3m 
$ tar xzvf mutt.tar.gz
$ mv mutt/* ~/
$ ln -s ~/.mutt/dot_muttrc ~/.muttrc

要更改的东西
=============

priv.rc里面的配置（主要是路径和信箱名称）可以根据自己需要更改。各种rc配置文件里面的邮箱密码改为自己的即可。
