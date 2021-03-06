## Linux下的ps命令使用

ps命令是最基本同时也是非常强大的进程查看命令。使用该命令可以确定有哪些进程正在运行和运行的状态、进程是否结束、进程有没有僵死、哪些进程占用了过多的资源等等。大部分信息都是可以通过执行该命令得到的。

**1. ps命令及其参数**

-e 显示所有进程  
-f 全格式  
-h 不显示标题  
-l 长格式  
-w 宽输出    
a 显示终端上的所有进程，包括其他用户的进程  
r 只显示正在运行的进程  

**2. 用ps查看进程**

* `$ ps -ef`  
* `$ ps aux`

**3. 查找某任务**

查找火狐任务，管道符“|”用来隔开两个命令，管道符左边命令的输出会作为管道符右边命令的输入

`$ ps -ef | grep firefox`  

**4. 杀死某个任务**

-s 9 制定了传递给进程的信号是９，即强制、尽快终止进程。1827则是ps查到的对应任务的PID

`$ kill -s 9 1827`
