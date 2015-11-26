# Gcc_1
----------------------------------------------------------------------------------------

一、应用程序 

1、  
/bin            二进制文件目录，启动系统时用到的程序  
/usr/bin        用户二进制文件目录，用户使用的标准程序  
/usr/local/bin  本地二进制文件目录，放软件安装的程序  

2、  
/usr/local 和 /opt 厂商及后续添加的应用程序    

二、头文件

1、  
/usr/include

2、  
/usr/include/sys  
/usr/include/linux  

3、  
/usr/include/X11  
/usr/include/c++  

4、用-I标志来指定非标准目录中的头文件  
gcc -o xx -I /usr/openwin/include xx.c

三、库文件  

1、  
/lib  
/usr/lib

2、  
libxxx.a静态库  
libxxx.so动态库  

3、  
指定库路径  
gcc -o xx xx.c /usr/lib/libm.a

4、  
-lm 表示指定路径下libm.so(优先)或者libm.a  
gcc -o xx xx.c -lm  

5、  
用-L标志来指定非标准目录中的头文件  
gcc -o xx -L /usr/openwin/lib xx.c -lX11  
