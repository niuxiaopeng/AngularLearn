# 如何构建测试环境，对HTML随时都可以调试？

[Browsersync的安装及使用方法][1]

[1]:https://www.cnblogs.com/hess/p/6483373.html

## Browsersync介绍

> Browsersync是浏览器同步测试工具，Browsersync能让浏览器实ß时、快速响应文件更改（html、js、css、sass、less等）并自动刷新页面。省去手动F5的事件，更重要的是 Browsersync可以同时在PC、平板、手机等设备下进项调试。即在任何一设备上操作，其他设备也随之改变，大大提高了测试效率。效果图：

### 自动刷新
### 各浏览器同步测试

## Browsersync安装

> 1）Global Install （全局安装）

> 如果你想在任何目录的命令行中运行Browsersync，可用这个命令进行全局安装，如果以下的命令不好使，请在命令前面添加sudo，输入密码，进行更高权限的安装。

    npm install -g browser-sync

> 2）Local Install （本地安装）

> 推荐这种方式来安装 Browsersync - 通过本地安装到每个项目。这种方式的可以使依赖被添加到你的package.json文件里（gulp或grunt构建方式）

    npm install browser-sync --save-dev

## 启动Browsersync

> 如果你只需要将css文件修改后同步到浏览器里，只需要在命令行里输入即可

### 静态网站

    // --files 路径是相对于运行该命令的项目（目录） 
    browser-sync start --server --files "css/*.css"

> 监听多个类型的文件，需要用逗号隔开。例如我们再加入一个.html文件

    // --files 路径是相对于运行该命令的项目（目录） 
    browser-sync start --server --files "css/*.css, *.html"
    // 如果你的文件层级比较深，您可以考虑使用 **（表示任意目录）匹配，任意目录下任意.css 或 .html文件。 
    browser-sync start --server --files "**/*.css, **/*.html"

> 运行命令后，Browsersync将创建一个本地服务器并自动打开你的浏览器后访问http://localhost:3000地址，这一切都会在命令行工具里显示。

# 强哥的命令：browser-sync start -s -f *.*

## 没有记录的内容

### 动态网站

### Browsersync+gulp

## 如果想获取这两个内容，请点击[这里][2]

[2]:https://www.cnblogs.com/hess/p/6483373.html






