# vue-oa

> 这是一个极简的 vue admin 管理后台。它只包含了 Element UI & axios & iconfont & permission control & lint，这些搭建后台必要的东西。

[线上地址](https://github.com/Whaojie521/vue-oa)

[国内访问](https://panjiachen.gitee.io/vue-admin-template)

目前版本为 `v4.0+` 基于 `vue-cli` 进行构建


## Build Setup

```bash
# 克隆项目
git clone https://github.com/Whaojie521/vue-oa

# 进入项目目录
cd vue-oa

# 安装依赖
npm install

# 建议不要直接使用 cnpm 安装以来，会有各种诡异的 bug。可以通过如下操作解决 npm 下载速度慢的问题
npm install --registry=https://registry.npm.taobao.org

# 启动服务
npm run dev
```

浏览器访问 [http://localhost:9528](http://localhost:9528)

## 发布

```bash
# 构建测试环境
npm run build:stage

# 构建生产环境
npm run build:prod
```

## 其它

```bash
# 预览发布环境效果
npm run preview

# 预览发布环境效果 + 静态资源分析
npm run preview -- --report

# 代码格式检查
npm run lint

# 代码格式检查并自动修复
npm run lint -- --fix
```



# 代码目录结构

## src 源代码

### api

服务端 api 调用的封装

### layout

页面布局

### views

路由页面文件

### router

路由配置信息

### store

vuex

## mock 服务器

此目录中的内容时临时测试服务器数据，实际开发时无用

## 用户登录页

1. 点击登录按钮之后会派发一个 action
2. 调用 api 文件夹中的登录接口发送一个 post 请求
3. 获取数据之后提交 commit 设置 state 中的 token 值
4. 在本地 cookie 中存储 token
5. 页面跳转
