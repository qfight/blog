# qfight 博客工程使用说明


### 安装

````
    npm install -g hexo //全局安装hexo
    
    npm install         //安装工程依赖包
````


### 使用

-----------

#### 本地启动

````
    npm start 或 hexo s -w -p 5555
````

此时会启动一个静态server在5555端口,本地访问: http://127.0.0.1:5555 即可

#### 创建文章

````
    hexo new [layout] <title>
````
layout顾名思义,指的是创建的文章的布局.可以不指定,默认为站点配置文件_config.yml的layout配置.
执行命令之后会发现有日志打印:
````
    INFO Created: __dirname/source/_post/[title].md
````
所以,直接在source/_post目录下创建md文件,也是没有问题的

#### 编辑文章/标签 等

https://hexo.io/zh-cn/docs/writing.html  
参考上面链接

#### 构建

``````
    npm run build 或  hexo g
``````

构建: 该命令将会把source/_post目录下的markdown文件编译成为html并且放在了public目录下

#### 发布

``````
    npm run deploy 或 hexo deploy
``````

发布: 将build产物,push到blog工程的gh-pages分支.需要注意的是,记得提交源代码到master分支

### 说明
 
上述提到的本地server启动,构建以及发布.可以参考,package.json脚本和_config.yml文件中的deploy部分.

hexo官网: https://hexo.io/


### 关于hexo主题

当前主题是NexT: http://theme-next.iissnan.com/

hexo主题可以随意更换,主题文件直接放在themes目录下,修改根目录下的_config.yml中的theme字段的值为对应主题即可.修改主题的配置,需要修改主题目录下的_config.yml文件.
明确一个概念,根目录下的_config.yml叫站点配置文件,主题目录下的_config.yml叫主题配置文件.