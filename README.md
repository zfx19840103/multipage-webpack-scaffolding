# 多页面webpack脚手架+npm发布
本脚手架适合做官网之类的多页面的应用


## Build Setup

``` bash
# 安装依赖
npm install

# 开发的时候在本地启localhost:8080，并开始热加载
npm run dev

# production的发布时打包
npm run build

```


## 目录结构

```

└─src                                      // src 文件夹
│    ├─pages                               // 页面文件夹
│    │  ├─about
│    │  │      about.html
│    │  │      about.js
│    │  │      about.less
│    │  │
│    │  ├─contact
│    │  │      contact.css
│    │  │      contact.html
│    │  │      contact.js
│    │  │
│    │  └─home
│    │          index.html
│    │          index.js
│    │          index.less
│    │
│    └─tools                          // 工具文件夹
│            utils.js
│
│  .babelrc                         // babel的配置文件
│  .eslintignore
│  .eslintrc.js                     // eslint的配置文件
│  .gitignore
│  ecosystem.config.js              // pm2 deploy的配置文件
│  package.json
│  page.config.js                   // 页面的配置文件
│  README.md
│  webpack.config.dev.js            // 开发环境的webpack配置文件
│  webpack.config.prod.js           // 生成环境的webpack配置文件
         

```

## 开发流程

如果增加新页面，只需两步，不需要改webpack等配置文件

1. 在pages中新增一个文件夹
2. 在page.config.js中添加这个页面的信息即可

比如
```
  {
    name: 'contact',
    html: 'contact/contact.html',
    jsEntry: 'contact/contact.js'
  }

```
## npm发布流程

1，注册npm账户，注册地址：https://www.npmjs.com/
2，验证邮箱（这一步相当重要，也许会遇到意想不到的问题导致发布失败）
3，npm init初始化工程，并编写代码（package.json介绍，包名命名规则）
4，登录npm账户（注意切换镜像，用淘宝镜像是不行的；首次和非首次登录）
5，npm publish发布npm包（包名问题；如何忽略不想上传的部分文件）
6，查看并测试使用npm包
7，更新npm包版本（npm的版本管理规则）
8，撤销已发布的npm包（如何强制撤销）
9，常见问题及解决方法（镜像问题，登录失败，验证邮箱，包名重复/存在相似等）
         
