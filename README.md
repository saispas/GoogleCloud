# GoogleCloud
设置独立SSH密码

1、首先使用WEB自带SSH连接上去，依次输入以下命令 
 
    sudo -i 
  
    vi /etc/ssh/sshd_config
  
2、找到

    PermitRootLogin no 改成 PermitRootLogin yes
    
    PasswordAuthentication no 改成 PasswordAuthentication yes
    
按 ESC 输入 :wq 保存退出

3、重启SSH服务

    输入 service sshd restart

重新使用WEB自带的SSH连接上去，依次以下命令
    sudo -i
    passwd
会提示直接输入新密码
再输入一次新密码
两次新密码输入确认后，密码提示成功。
