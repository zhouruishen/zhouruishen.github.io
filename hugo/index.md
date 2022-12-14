# 用Hugo搭建网站


# 前言 

Hugo 是一款基于 Go 语言而实现的静态网站生成器，具有简单易用、高效易扩展、快速部署的特点。
这里先给出 Hugo 的中英文官方文档，方便大家遇到问题时查阅：
> https://www.gohugo.org/          '中文档案'

> https://gohugo.io/documentation/ '英文档案'

# 搭建过程
## 1.通过下方链接下载安装包 
>  https://github.com/gohugoio/hugo/releases

![](/images/p5.png)



通过指令下载
```markdown
wget https://github.com/gohugoio/hugo/releases/download/v0.108.0/hugo_0.108.0_Linux-64bit.tar.gz
```

## 2.解压配置hugo
下载完成后解压,将路径复制到/usr/local/bin目录下，使用sudo version查看是否安装成功
```markdown
tar -zxf hugo_0.108.0_Linux-64bit.tar.gz
cp ./usr/local/bin/
```
用'hugo --version'命令查看是否安装成功
```markdown
hugo --verison
```
## 3.创建一个新站点
```markdown
hugo new site my_website
```
![](/images/p6.png)

## 4.下载主题
git clone命令克隆主题到文件
```markdown
cd my_website
git clone '下载连接' /theme
```
## 5.配置文件
在主题中查看配置文件，将其复制到config.toml文件中
```markdown
vim config.tom
```
![](/images/p7.png)

## 6.测试
设置好主题之后，就可以进行预览了！使用如下命令启动 Hugo 服务器，然后进入  
> http://localhost:1313  

即可进行预览
```markdown
hugo server --buildDrafts
```
出现如下界面，就安装完成啦～
![](/images/p8.png)

