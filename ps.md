Linux ps命令用于显示当前进程 (process) 的状态。

### 参数
ps 的参数非常多, 在此仅列出几个常用的参数并大略介绍含义
* -A 列出所有的行程
* -w 显示加宽可以显示较多的资讯
* -au 显示较详细的资讯
* -aux 列出目前所有的正在内存当中的程序

* au(x) 输出格式 :
USER PID %CPU %MEM VSZ RSS TTY STAT START TIME COMMAND
* USER: 行程拥有者
* PID: pid
* %CPU: 占用的 CPU 使用率
* %MEM: 占用的记忆体使用率
* VSZ: 占用的虚拟记忆体大小
* RSS: 占用的记忆体大小
* TTY: 终端的次要装置号码 (minor device number of tty)
* STAT: 该行程的状态:
* D: 无法中断的休眠状态 (通常 IO 的进程)
* R: 正在执行中
* S: 静止状态
* T: 暂停执行
* Z: 不存在但暂时无法消除
* W: 没有足够的记忆体分页可分配
* <: 高优先序的行程
* N: 低优先序的行程
* L: 有记忆体分页分配并锁在记忆体内 (实时系统或捱A I/O)
* START: 行程开始时间
* TIME: 执行的时间
* COMMAND:所执行的指令  

### ps -u root //显示root进程用户信息  

### ps -ef //显示所有进程信息，连同命令行  

### 将目前属于您自己这次登入的 PID 与相关信息列示出来

命令：

　　ps -l

### 进程启动的线程
ps -Lf 4551