# 在Linux中安装git


# git官网下载地址

>  https://git-scm.com/download/linux

## 一、方法一
### 1.在linux上直接用yum安装git，方法很简单，不过下载的版本比较落后
```markdown
yun -y install git
```
![](/images/p1.png)
### 2.输入git --version查看git是否安装成功
```markdown
git --version
```
## 二、方法二
### 1.先卸载linux自带的git
```markdown
yum remove git
```
### 2.安装git最新安装包，若需要其他版本可以官网自己复制连接
```markdown
wget https://www.kernel.org/pub/software/scm/git/git-2.39.0.tar.gz
```
### 3.解压安装包
```markdown
tar -zxvf git-2.39.0.tar.gz
```
### 4.安装git之前要先安装依赖
```markdown
yum install -y curl-devel expat-devel gettext-devel openssl-devel zlib-devel
yum install -y gcc perl-ExtUtils-MakeMaker
```
### 5.编译源码
```markdown
cd git-2.39.0.tar.gz    
make prefix=/usr/local/git
```
`![](/images/p2.png)
### 6.安装git
```mardown
make prefix=/usr/local/git 
```
`![](/images/p3.png)
### 7.配置环境
```markdown
sudo vim /etc/profile
```
### 8.在底部加上
```markdown
export PATH=$PATH:/usr/local/git/bin
```
### 9.刷新环境变量
```markdown
source /etc/profile
```
### 10.查看git是否安装成功
```markdown
git --version
```
![](/images/p4.png)

这样GIT就安装完了！！！！

