# shell_setting

## lrzsz安装

copy from:https://www.jianshu.com/p/2f131136e385

rz/sz卡死问题解决
1. 安装lrzsz
brew install lrzsz

2. 下载iterm2-zmodem：
下载地址：https://github.com/mmastrac/iterm2-zmodem

  将解压后的sh脚本移动到    /usr/local/bin/下

  然后给两个脚本配置执行权限

  sudo chmod 777 /usr/local/bin/iterm2-*

  或者 sudo chomd u+x /usr/local/bin/iterm2-*    应该都可以  我用的下面这个

3. 配置triggers
    打开Item2，点击preferences → profiles，选择某个profile，如Default，之后继续

    选择  advanced → triggers，添加编辑添加如下triggers：

    Regular ExpressionActionParameters

    rz waiting to receive.\*\*B0100Run

    Silent Coprocess

    /usr/local/bin/iterm2-send-zmodem.sh

    \*\*B00000000000000

    Run Silent Coprocess

    /usr/local/bin/iterm2-recv-zmodem.sh

具体配置如下图：


