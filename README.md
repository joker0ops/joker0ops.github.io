# 博客

## Example site modified from https://github.com/gohugoio/hugoBasicExample

## 博客开发过程
### 1. 安装Hugo-extended
### 2. 使用 **hugo version** 命令检查当前hugo版本是不是extended版本
### 3. 进入工作目录，使用 **hugo new site [仓库名]** 命令来指定需要创建的博客站点，hugo将在该站点目录下生成一系列的文件用于博客开发
### 4. 进入站点目录，查看目录结构：
```javascript
joker@joker-virtual-machine:~/Code/Blog $ tree -L 1
.
├── archetypes      // 存放Markdown文章的模板，初始为Hugo默认的模板文件
├── assets      // 保存所有需要通过 Hugo Pipes 处理的资源，只有那些 .Permalink 和 .RelPermalink 引用的文件会发布到 public 目录中
├── config.yaml     // 个人博客的配置文件
├── content     // 博客文章的存放位置
├── data        // 存放Hugo数据
├── layouts     // 存放自定义的view，可以为空
├── LICENSE
├── public -> /home/joker/Code/Repository/joker0ops.github.io       // 使用hugo命令对你编写的Markdown文件进行解析后会生成的一系列文件都会存放在该目录
├── README.md
├── resources       // 用于缓存某些文件来提高生成效率
├── static      // 存放图像、CNAME、css、js等资源，发布后该目录下所有资源将处于网页根目录
└── themes      // 存放你安装的 Hugo 主题
// 对于public文件夹我使用了一个软连接直接连接到我的GitHub本地库，后面会讲到
```
### 5. 使用 **git clone** 下载相应的Hugo主题到themes文件夹，再把所安装的主题的exampleSite下的所有文件复制并覆盖到站点目录下

### 6. 在站点目录下使用 **hugo server** 命令运行站点，查看网站效果

### 7. 在GitHub上创建username.github.io仓库，并使用 **git clone {ssh-url}** 克隆本地仓库

### 8. 使用 **hugo new post/{文件夹名}/index.md** 创建一篇新的博客或博客目录

### 9. 删除站点目录下的public文件夹使用 **sudo ln -s 本地GitHub仓库目录 站点目录/public** 建立软链接

### 10. 使用 **hugo** 命令将编写的博客编译为HTML文件及其他支持文件存放入public中

### 11. **cd**进入本地GitHub仓库，发现生成的HTML文件都在其中

### 12. 使用 **git add \*** 将所有修改过的文件添加进入暂存区

### 13. 使用 **git commit -m "提交说明"** 提交修改

### 14. 使用 **git remote -v** 查看远程库别名

### 15. 使用 **git push 别名 分支名** 将本地分支推送到远程库

## 配置解析
