## 本仓地址

https://github.com/Carter-luo/Carter-luo.github.io.git

## 访问主页
[https://carter-luo.github.io/](https://carter-luo.github.io/)


1. **安装 Node.js**：
    
    - 访问 [Node.js 官网](https://nodejs.org/) 下载并安装 Node.js。
        
    - 安装完成后，在命令行中运行 `node -v` 和 `npm -v`，确认安装成功。

目前版本是
```
node -v
v22.13.1

npm -v
10.9.2
```



2. **安装 Git**：
    
    - 对于 Windows 系统，访问 [Git 官网](https://git-scm.com/) 下载并安装 Git。
        
    - 安装完成后，在命令行中运行 `git --version`，确认安装成功。
        
    - 对于 Linux 系统，可以使用以下命令安装 Git：
        
        - Ubuntu/Debian: `sudo apt-get install git`
            
        - CentOS/Fedora: `sudo yum install git`
            
3. **安装 Hexo**：
    
    - 在命令行中运行以下命令安装 Hexo：
        
        bash复制
        
        ```bash
        npm install -g hexo-cli
        ```
        
    - 安装完成后，运行 `hexo -v`，确认安装成功。
```
hexo -v
hexo-cli: 4.3.2
os: win32 10.0.17763 undefined
node: 22.13.1
acorn: 8.14.0
ada: 2.9.2
amaro: 0.2.0
ares: 1.34.4
brotli: 1.1.0
cjs_module_lexer: 1.4.1
cldr: 46.0
icu: 76.1
llhttp: 9.2.1
modules: 127
napi: 9
nbytes: 0.1.1
ncrypto: 0.0.1
nghttp2: 1.64.0
nghttp3: 1.6.0
ngtcp2: 1.9.1
openssl: 3.0.15+quic
simdjson: 3.10.1
simdutf: 5.6.4
sqlite: 3.47.2
tz: 2024b
undici: 6.21.1
unicode: 16.0
uv: 1.49.2
uvwasi: 0.0.21
v8: 12.4.254.21-node.22
zlib: 1.3.0.1-motley-82a5fec   
```

### 博客站点初始化

4. **创建博客工作区**：
    
    - 选择一个空文件夹作为博客的工作区。
        
    - 在该文件夹中打开命令行，运行以下命令初始化 Hexo 博客：
        
        bash复制
        
        ```bash
        hexo init
        ```

    - 运行以下命令安装依赖包：
        
        bash复制
    
        ```bash
        npm install
        ```
        
5. **生成静态文件**：
    
    - 在博客工作区中运行以下命令生成静态文件：
        
        bash复制
        
        ```bash
        hexo generate
        ```
生成

```

E:\vscode_code\Personal\Active\my-hexo-blog>        hexo generate
INFO  Validating config
INFO  Start processing
INFO  Files loaded in 606 ms
INFO  Generated: archives/index.html
INFO  Generated: archives/2025/index.html
INFO  Generated: archives/2025/02/index.html
INFO  Generated: index.html
INFO  Generated: js/jquery-3.6.4.min.js
INFO  Generated: fancybox/jquery.fancybox.min.css
INFO  Generated: css/style.css
INFO  Generated: fancybox/jquery.fancybox.min.js
INFO  Generated: js/script.js
INFO  Generated: css/images/banner.jpg
INFO  Generated: 2025/02/11/hello-world/index.html
INFO  11 files generated in 730 ms

E:\vscode_code\Personal\Active\my-hexo-blog>
```
1. **本地预览**：
    
    - 运行以下命令启动本地服务器预览博客：
        
        bash复制
        
        ```bash
        hexo server
        ```
        
    - 访问
```
    http://localhost:4000
```
     查看博客预览效果。
        

### GitHub 建站

2. **创建 GitHub 仓库**：
https://github.com/Carter-luo/Carter-luo.github.io.git
    - 在 GitHub 上创建一个仓库，仓库名称必须为 `yourusername.github.io`，其中 `yourusername` 是你的 GitHub 用户名。
        
3. **安装部署插件**：
    
    - 在博客工作区中运行以下命令安装 Hexo 的 Git 部署插件：
        
        bash复制
        
        ```bash
        npm install hexo-deployer-git --save
        ```

成
```
E:\vscode_code\Personal\Active\my-hexo-blog>        npm install hexo-deployer-git --save

added 9 packages, and audited 230 packages in 29s

34 packages are looking for funding
  run `npm fund` for details

found 0 vulnerabilities

E:\vscode_code\Personal\Active\my-hexo-blog>
```

4. **配置部署信息**：
    
    - 编辑 `_config.yml` 文件，在 `deploy` 模块中添加以下内容：
        
        yaml复制
        
        ```yaml
        deploy:
          type: git
          repo: https://github.com/yourusername/yourusername.github.io.git
          branch: main
        ```
        
5. **部署到 GitHub**：
    
    - 运行以下命令将博客推送到 GitHub：
        
        bash复制
        
        ```bash
        hexo deploy
        ```


报错

```
C:\code_vscode\Personal\Active\my-hexo-blog>        hexo deploy
FATAL
YAMLException: duplicated mapping key (107:1)

 104 |
 105 | # Deployment
 106 | ## Docs: https://hexo.io/docs/o ...
 107 | deploy:
-------^
 108 |   type: ''
    at generateError (C:\code_vscode\Personal\Active\my-hexo-blog\node_modules\js-yaml\lib\loader.js:183:10)
    at throwError (C:\code_vscode\Personal\Active\my-hexo-blog\node_modules\js-yaml\lib\loader.js:187:9)
    at storeMappingPair (C:\code_vscode\Personal\Active\my-hexo-blog\node_modules\js-yaml\lib\loader.js:358:7)
    at readBlockMapping (C:\code_vscode\Personal\Active\my-hexo-blog\node_modules\js-yaml\lib\loader.js:1173:9)
    at composeNode (C:\code_vscode\Personal\Active\my-hexo-blog\node_modules\js-yaml\lib\loader.js:1441:12)
    at readDocument (C:\code_vscode\Personal\Active\my-hexo-blog\node_modules\js-yaml\lib\loader.js:1625:3)
    at loadDocuments (C:\code_vscode\Personal\Active\my-hexo-blog\node_modules\js-yaml\lib\loader.js:1688:5)
    at Object.load (C:\code_vscode\Personal\Active\my-hexo-blog\node_modules\js-yaml\lib\loader.js:1714:19)
    at Hexo.yamlHelper (C:\code_vscode\Personal\Active\my-hexo-blog\node_modules\hexo\dist\plugins\renderer\yaml.js:22:30)
    at Hexo.tryCatcher (C:\code_vscode\Personal\Active\my-hexo-blog\node_modules\bluebird\js\release\util.js:16:23)
    at Hexo.<anonymous> (C:\code_vscode\Personal\Active\my-hexo-blog\node_modules\bluebird\js\release\method.js:15:34)
    at C:\code_vscode\Personal\Active\my-hexo-blog\node_modules\hexo\dist\hexo\render.js:73:28
    at tryCatcher (C:\code_vscode\Personal\Active\my-hexo-blog\node_modules\bluebird\js\release\util.js:16:23)
    at Promise._settlePromiseFromHandler (C:\code_vscode\Personal\Active\my-hexo-blog\node_modules\bluebird\js\release\promise.js:547:31)
    at Promise._settlePromise (C:\code_vscode\Personal\Active\my-hexo-blog\node_modules\bluebird\js\release\promise.js:604:18)
    at Promise._settlePromise0 (C:\code_vscode\Personal\Active\my-hexo-blog\node_modules\bluebird\js\release\promise.js:649:10)
    at Promise._settlePromises (C:\code_vscode\Personal\Active\my-hexo-blog\node_modules\bluebird\js\release\promise.js:729:18)
    at _drainQueueStep (C:\code_vscode\Personal\Active\my-hexo-blog\node_modules\bluebird\js\release\async.js:93:12)
    at _drainQueue (C:\code_vscode\Personal\Active\my-hexo-blog\node_modules\bluebird\js\release\async.js:86:9)
    at Async._drainQueues (C:\code_vscode\Personal\Active\my-hexo-blog\node_modules\bluebird\js\release\async.js:102:5)
    at Async.drainQueues (C:\code_vscode\Personal\Active\my-hexo-blog\node_modules\bluebird\js\release\async.js:15:14)
    at process.processImmediate (node:internal/timers:491:21)

```

原因
`deploy`这样的关键词在`_config.yml`文件中只能出现一次。YAML文件是一种数据序列化格式，它要求每个键（key）在同一个层级中是唯一的。如果同一个键被重复定义，就会导致解析错误，就像你遇到的`duplicated mapping key`错误。


成功
可以从仓库查看到文件的上传情况。以仓库名称作为域名访问即可成功查看到博客界面：`https://username.github.io`。


### 创建与删除文章

6. **创建文章**：
    
    - 在博客工作区中运行以下命令创建文章：
        
        bash复制
        
        ```bash
        hexo new "文章标题"
        ```
        
    - 文章文件将生成在 `source/_posts` 目录下。
        
7. **删除文章**：
    
    - 直接删除 `source/_posts` 目录下的文章文件即可。
        

### 更换主题

8. **选择主题**：
    
    - 访问 [Hexo 主题官网](https://hexo.io/themes/) 或在 GitHub 上搜索 Hexo 主题。
        
    - 选择一个你喜欢的主题，并按照其文档进行安装和配置。
        

### 其他细节

9. **修改作者头像和标签页图标**：
    
    - 在主题的 `source` 目录中替换相关图片文件。
        
10. **修改本地服务器端口号**：
    
    - 编辑 `package.json` 文件，修改 `scripts` 部分的端口号：
        
        JSON复制
        
        ```json
        "scripts": {
          "build": "hexo generate",
          "clean": "hexo clean",
          "deploy": "hexo deploy",
          "server": "hexo server -p 4001"
        }
        ```
        
11. **数学公式渲染**：
    
    - 如果需要在文章中使用数学公式，可以参考相关插件或配置。
        

按照这篇教程的步骤操作，你应该能够顺利搭建起自己的静态博客。如果在过程中遇到任何问题，可以随时参考教程中的详细说明或在评论区提问。祝你搭建顺利！