# 实现一个高仿的 cnode 社区
效果链接：https://liujianli000.github.io/cnode/#/
<br>


## 项目模块组件

- Header模块：头部的 logo 和导航栏
- PostList模块：主页的发布列表
- Article模块：文章的详情部分
- Slide侧边栏模块：包含作者基本信息，作者最近主题，作者最近回复
- UserInfo模块：用户个人中心模块
- Pagination：分页组件的开发

## 项目中使用到的技术栈

- vue.js计算属性
- vue.js的内置指令和事件绑定
- vue.js的自定义事件和触发
- vue-router路由的跳转和监听
- 父子组件之间的数据传递
- Axios中的get请求

## 遇到的问题

- 侧边栏中，单击链接时，左边文章详情页内容不发生变化

原因：在同一个路由内检测不到变化，所以应该要实现路由跳转
解决：在Article组件中，添加监听路由变化的组件

主要代码如下：
```
watch: {  
    $route(to, from) {
      this.getArticleData();
    }
}  
```
