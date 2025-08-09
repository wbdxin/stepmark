# Stepmark
### 预备环境:  
&nbsp;&nbsp;注册github账号  
&nbsp;&nbsp;本机安装git,ssh,vim  

## 初始配置  
 
生成SSH Key:  
&nbsp;&nbsp;客户端执行:ssh-keygen -t rsa -b 4096 -C "your_email@example.com".  
&nbsp;&nbsp;使用你的邮箱地址代替your_email@example.com  
&nbsp;&nbsp;按3次回车,使用默认设置  

    the id_rsa and id_rsa.pub will save at ~/.ssh。
2. 将公钥添加到GitHub:
打开 id_rsa.pub 文件, 复制其中的内容。
登录GitHub, 点击右上角头像, 选择"Settings"。
在左侧边栏选择"SSH and GPG keys"。
点击"New SSH key" 按钮。
在"Title" 字段输入一个名称, 方便区分不同的SSH Key, 比如"My SSH Key"。
在"Key" 字段粘贴刚才复制的公钥内容。
点击"Add SSH key" 按钮。﻿
3. 测试SSH连接:
在Git Bash中输入 ssh -T git@github.com。
如果提示 Hi username! You've successfully authenticated, but GitHub does not provide shell access. , 则表示连接成功。( username 是你的GitHub用户名)
如果提示需要输入密码或连接失败, 则需要检查步骤1和步骤2, 确保公钥正确添加到GitHub, 并且私钥没有泄露。
4. 使用SSH协议进行Git操作:
在克隆仓库时, 选择 SSH 协议的clone地址, 例如 git@github.com:username/repository.git 。
在使用 git clone, git pull, git push 等命令时, Git会使用SSH协议进行认证和数据传输。

## add pad access by ssh
