### AutoHotKey 学习

http://ahkcn.sourceforge.net/docs/Tutorial.htm

#### 例子
* win+空格，跳转到google(#表示win键，space表示空格，::是按键和命令的分隔符)
~~~
#space::Run www.google.com 
~~~

* Run命令：启动程序、文档、URL或快捷方式(如果要运行qq，需要将qq.exe加入环境变量中，否则需要完整路径)，
    %A_ProgramFiles%表示内置变量，也就是"C:\Program Files",可以在所有电脑上通用。
    且内置变量和命令，诸如run、send都不区分大小写
~~~
Run Notepad
Run C:\My Documents\Address List.doc
Run %A_ProgramFiles%\My Shortcut.lnk
Run www.yahoo.com
Run mailto:someone@somedomain.com
~~~

* 在一个热键中执行多个命令(命令换行，并在最后一行加上return)
~~~
#n::
Run www.google.com
Run www.baidu.com
return 
~~~

* Send命令：在活动窗口键入字符(中文乱码，将ahk文件编码改为Unicode(Unicode是记事本的编码，在idea中显示为UTF-16LE,应该也是UTF8-BOM))
    {Enter}表示键入回车换行
~~~
^!s::
Send "这是一个测试命令,{Enter}测试换行"
return
~~~
