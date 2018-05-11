# JAVA环境变量配置详解  

-----

JAVA环境变量JAVA_HOME、CLASSPATH、PATH设置详解  

 Windows下JAVA用到的环境变量主要有3个，**JAVA_HOME、CLASSPATH、PATH。**  

### 1. JAVA_HOME  
	 指向的是JDK的安装路径，如C:\jdk1.5.0_06，在这路径下你应该能够找到bin、lib等目录。    
	 
( 注意JDK和Eclipse必须同位数Bit才可以使用，不能是不同位数的程序，已实践，不然要报错无法使用；如需卸载JDK，JDK不能直接删除文件夹，要使用卸载方式，不然无法再使用JDK或无法卸载，只有重新安装OS才能使用了，以前遇过 )  
> JAVA_HOME=C:\jdk1.5.0_06  
	  
### 2. PATH  
环境变量原来Windows里面就有，你只需修改一下，使他指向JDK的bin目录，这样你在控制台下面编译、执行程序时就不需要再键入一大串路径了。设置方法是保留原来的PATH的内容，并在其中加上%JAVA_HOME%\bin  

*(注，如果你对DOS批处理不了解，你可能不明白%%引起来的内容是什么意思；其实这里是引用上一步设定好的环境变量JAVA_HOME，你写成x:\JDK_1.4.2也是可以的；你可以打开一个控制台窗口，输入echo %JAVA_HOME%来看一下你的设置结果)*    

> PATH=%JAVA_HOME%\bin;%PATH%  

同样，%PATH%是引用以前你设置的PATH环境变量，你照抄以前的值就行了。  
	 
### 3. CLASSPATH  
环境变量我放在最后面，是因为以后你出现的莫名其妙的怪问题80%以上都可能是由于CLASSPATH设置不对引起的，所以要加倍小心才行。  
> CLASSPATH=.;%JAVA_HOME%\lib;%JAVA_HOME%\lib\tools.jar  


