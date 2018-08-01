
<div align="center">
  <img width="150"eight="150"  src="https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1533058717761&di=161d19751a8536d50fa99069e12af046&imgtype=0&src=http%3A%2F%2Fimage.coolapk.com%2Fdiscovery%2F2016%2F1009%2F480069_1476026104_6583.png">
</div>

# vue-music

> Jasonccj音乐播放器

## Build Setup

``` bash
npm install  -->  npm run dev

```

## 概览 项目目录结构

初始化,随项目开发不断完善中

```
.
└── src
    ├── api  空文件夹,待开发
    ├── common 
        ├── fonts 字体,及一些icon基本文件
        ├── image 默认图片文件
        ├── js 相关js文件
        ├── stylus 全局css相关配置文件
    ├── components 自定义组件
    ├── router  路由配置
    ├── store  空文件夹,待开发
```

## 第一章

### 页面入口及header组件的开发
 <meta name="viewport"                        移动端常用的基本配置

"dependencies": {
    "babel-runtime": "^6.0.0",                对es的语法做一些转译
     "fastclick": "^1.0.6"                    解决移动端点击300ms的延迟
},               

"devDependencies": {
    "babel-polyfill": "^6.2.0",               对es6的一些api做转译

m--hader                                      header组件

### 路由配置及顶导组件开发

4个组件界面,通过路由切换
main.js中注册路由 并在vue中引入
    import router from './router'

router/index.js 配置及使用路由
    import Router from 'vue-router'
    Vue.use(Router)

通过 
routes: [{
      path: '/',         //默认首次进入
      redirect: '/recommend'
},{
    path: '/recommend',
    component: Recommend
}]
配置跳转路径

路由切换
<router-link tag="要渲染成什么dom,默认为a标签" to="跳转路由路径,例如:'/recommend'" ></router-link>
css 中 &.router-link-active 当路由被触发时,可做的css动作

路由显示
<router-view></router-view>
