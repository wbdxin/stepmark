# Stepmark
### 预备环境:  
- 注册github账号  
- 本机安装git,ssh,vim  

# 初始配置  
 
### 生成SSH Key:  
- 客户端执行:ssh-keygen -t rsa -b 4096 -C "your_email@example.com".  
- 使用你的邮箱地址代替your_email@example.com  
- 按3次回车,使用默认设置  
- id_rsa和id_rsa.pub文件保存在~/.ssh  
### 将公钥添加到GitHub:
- 打开 id_rsa.pub 文件, 复制其中的内容。
- 登录GitHub, 点击右上角头像, 选择"Settings"。
- 在左侧边栏选择"SSH and GPG keys"。
- 点击"New SSH key" 按钮。
- 在"Title" 字段输入一个名称, 方便区分不同的SSH Key, 比如"My SSH Key"。
- 在"Key" 字段粘贴刚才复制的公钥内容。
- 点击"Add SSH key" 按钮。﻿
### 测试SSH连接:
- 在Git Bash中输入 ssh -T git@github.com。
- 如果提示 Hi username! You've successfully authenticated, but GitHub does not provide shell access. , 则表示连接成功。( username 是你的GitHub用户名)
- 如果提示需要输入密码或连接失败, 则需要检查步骤1和步骤2, 确保公钥正确添加到GitHub, 并且私钥没有泄露。
### 使用SSH协议进行Git操作:
- 在github创建库,并获取ssh协议链接，例如:git@github.com:username/stepmark.git
- 在客户端执行git clone git@github.com:username/stepmark.git
- 在不同客户端编辑文件前，先执行git pul，从githuhb拉取最新内容
- 编辑需要的文件
- 执行git add . 将变更加到本地
- 执行git commit -m "comment" 将变更进行提交
- 执行git push 使提交的变更生效 
## add pad access by ssh
