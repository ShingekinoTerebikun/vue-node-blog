### 环境准备

- Node.js v14.15.5
- MongoDB v4.2.17

### 安装MongoDB数据库

进入[官网](https://www.mongodb.com/try/download/community)下载，版本是4.2.17，平台是Windows，安装包为msi格式

### 项目开发

#### 1. 克隆项目至本地：

```sh
$ git clone git@github.com:miqilin21/vue-blog.git
$ cd vue-blog
$ yarn
```

#### 2. 安装前后台(admin、web)及后端(server)项目依赖：

```sh
$ yarn install-all
```

#### 3. 运行前后台(admin、web)及后端(server)项目：

```sh
$ yarn serve-all
```

#### 4. 打开浏览器预览：

http://localhost:8080 打开前台本地页面；http://localhost:8088 打开后台本地页面。

第一次后台admin登陆时请先注册用户，登录后可以将注册按钮隐藏以防登录账户泄露。

### 后台管理系统

- 新增分类
- 分类列表(增删改查)

- 新增文章
- 文章列表(增删改查)

- 文章评论列表

- 新增友链
- 友链列表(增删改查)

- 留言列表

- 留言用户列表

- Markdown 编辑器集成
- 图片上传功能

- 新增用户
- 用户列表(增删改查)

- 通用增删改查接口实现(中间件 resourceMiddleware)

- 登录注册功能
- 登出功能
- 添加 jwt 校验（1. 用户名查找 2. 密码校验 3. 返回 token）
- 添加 http 拦截器（request、response)

### 博客系统

- 博客首页 UI
- 博客首页接口实现
- 博客归档页面 UI
- 博客归档页面接口实现
- 博客标签页面 UI
- 博客标签页面接口实现
- 博客文章页面 UI
- 博客文章页面接口实现
- 博客友链页面 UI
- 博客友链页面接口实现
- 博客留言页面 UI
- 博客留言页面接口实现

这里需要注意一点，评论页面回复他人评论采用的是你的QQ邮箱进行同步通知，需要在 `server/plugins/sendEmail.js` 中进行邮箱配置，如何获取QQ邮箱授权码见[此图](https://cdn.jsdelivr.net/gh/miqilin21/static@master/img/qq-shouquanma.png)。

### 项目打包部署

- web、admin 项目打包(根目录下运行 `yarn build-all` 命令)
- 域名购买
- 域名解析
- linux 云服务器购买
- git 安装, ssh key 添加
- pm2 进程管理
- ngnix 配置
- mongodb 配置
- mongodb 数据从本地迁移至服务器
- 七牛云 cdn 全站免费加速

线上服务器部署可参考这份[指南](https://www.yuque.com/lingqian-ceavu/gxhqpr)。

### 博客后台管理系统

![](https://miqilin-blog.oss-cn-shenzhen.aliyuncs.com/admin.gif)

### 博客系统

![](https://miqilin-blog.oss-cn-shenzhen.aliyuncs.com/web.gif)

### 欢迎 Star，Issues

- 您的 Star，是我不断更新维护的动力！！！
- 若在使用过程中，存在某些问题，欢迎 Issues

### To Do List

- 性能优化，图片需要压缩处理，预加载处理
- 给博文页面加上搜索功能
- 浏览器兼容问题，移动端适配。只用了自己电脑的谷歌 chrome 浏览器开发和手机适配效果，其他种种都没试，不过不建议移动端使用，电脑登陆效果更佳
- 解决 vue 的 seo 问题及刷新渲染页面抖动问题。先暂时做 vue 预渲染，不排除以后会做 vue 服务端渲染或 nuxt.js 服务端渲染
- 整理代码，拆分出组件。让结构更清晰，代码量更少
- 利用 typescript 重构整个项目
- 想到有意思的功能也会慢慢加上，持续开发中...
