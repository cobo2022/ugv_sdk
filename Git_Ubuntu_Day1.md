# 智元算法开发Day1：Ubuntu+Git核心笔记

## 一、Ubuntu终端高频命令

### 1. 快捷操作
- Ctrl+Alt+T: 打开终端
- Tab: 自动补全
- Ctrl+Shift+C/V: 终端复制粘贴
- Ctrl+C: 终止进程
- clear: 清屏

### 2. 核心命令
- 目录操作: `ls -l` / `cd ~/` / `cd ..` / `pwd` / `mkdir -p` / `rm -rf`（谨慎）
- 权限安装: `sudo` / `apt update` / `apt install` / `pip3 install --upgrade pip`
- 进程查看: `ps -ef | grep 进程名` / `df -h`

## 二、Git团队协作流程（智元规范）

1.  安装验证: `sudo apt install git -y` → `git --version`
2.  全局配置: `git config --global user.name/email/editor`
3.  核心操作: `git clone` → `git add` → `git commit -m`
4.  团队分支: `git checkout -b dev_用户名` → `git push -u origin 分支名` → `git pull origin main`
5.  冲突解决: 删除冲突标记 → `git add` → `git commit` → `git push`

## 三、踩坑点

1.  `rm -rf` 禁止用于系统目录，仅删除自己创建的文件
2.  `sudo` 输入密码时终端不显示，直接输入回车即可
3.  Git 注释必须清晰，分支名按 `dev_用户名` 命名，禁止直接操作 main 分支
4.  拉取代码前先提交本地修改，避免冲突
