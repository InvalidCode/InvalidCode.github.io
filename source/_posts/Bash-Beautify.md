---
title: Bash美化
date: 2016-09-03 13:45:14
tags: [Course]
category: [Linux]
toc: true
comments: true
---
## 范例
**`/etc/bash.bashrc`文件中添加:**
```
alias ls='ls --color=auto'
PS1='[\[\033[1;31m\]\u\[\033[0m\]@\[\033[1;32m\]\h \[\033[1;36m\]\W\[\033[0m\]]\$ '
```
**`～/.bashrc`文件中：**
```
alias ls='ls --color=auto'
PS1='[\u@\h \W]\$ '
```
**改为：**
```
alias ls='ls --color=auto'
PS1='[\[\033[1;31m\]\u\[\033[0m\]@\[\033[1;32m\]\h \[\033[1;36m\]\W\[\033[0m\]]\$ '
```

<!--more-->
## 语法 说明
`\[\033[1;31m\]`
* `ANSI`色彩控制语法。`\033`声明了转义序列的开始，然后是`[`开始定义颜色
* 第一组数字：亮度 (普通0, 高亮度1, 闪烁2)
* 第二组数字：顏色代码

`\[\033[0m\]`
* 关闭`ANSI`色彩控制，通常置于尾端

## 颜色 代码
* 30 black
* 31 red
* 32 green
* 33 yellow
* 34 blue
* 35 magenta
* 36 cyan
* 37 white

## 显示 内容
* \a     ASCII响铃字符 (07)
* \d     “周 月 日”格式的日期
* \D{format}   参数format被传递给strftime(3)来构造自定格式的时间并插入提示符中；该参数为空时根据本地化设置自动生成格式。
* \e     ASCII转义字符（ESC) (033)
* \h     主机名在第一个点号前的内容
* \H     完全主机名
* \j     shell当前管理的任务数
* \l     shell终端设备的基本名称
* \n     新行
* \r     回车
* \s     shell的名称，$0的基本名称
* \t     当前时间（24小时） HH:MM:SS
* \T     当前时间（12小时） HH:MM:SS
* \@     当前时间（12小时） am/pm
* \A     当前时间（24小时） HH:MM
* \u     当前用户名称
* \v     bash版本(如"2.00")
* \V     bash版本+补丁号(如"2.00.0")
* \w     当前工作目录
* \W     当前工作目录的基本名称
* \!     该命令的历史数（在历史文件中的位置）
* \#     该命令的命令数（当前shell中执行的序列位置）
* \$     根用户为"#"，其它用户为"$"
* \nnn   8进制数
* \\     反斜杠
* \[     表示跟在后面的是非打印字符，可用于shell的颜色控制
* \]     表示非打印字符结束

