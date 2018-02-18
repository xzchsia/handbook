# handbook
document

these files are collected from network


# android source
android web : http://www.androiddevtools.cn/

Android SDK proxy

1.启动 Android SDK Manager ，打开主界面，依次选择「Tools」、「Options...」，弹出『Android SDK Manager - Settings』窗口；

2.在『Android SDK Manager - Settings』窗口中，在「HTTP Proxy Server」和「HTTP Proxy Port」输入框内填入

	东软：mirrors.neusoft.edu.cn和80，
	
	郑州大学：mirrors.zzu.edu.cn 端口：80
	
并且选中「Force https://... sources to be fetched using http://...」复选框。设置完成后单击「Close」按钮关闭『Android SDK Manager - Settings』窗口返回到主界面；

3.依次选择「Packages」、「Reload」。

# git-ssh 配置和使用
1、设置Git的user name和email

    $ git config --global user.name "xxx"
	
    $ git config --global user.email "xxx@yyy.com"

2、生成密钥

    $ ssh-keygen -t rsa -C "xxx@yyy.com"
连续3个回车。如果不需要密码的话。
最后得到了两个文件：id_rsa和id_rsa.pub。

3、登陆Github, 添加 ssh 

    把id_rsa.pub文件里的内容复制到 SSH and GPG keys 里面添加

4、使用TortoiseGit的话，可以setting里面的network的SSH client里面
选择git的ssh，新版本的git地址在\Git\usr\bin\ssh.exe
