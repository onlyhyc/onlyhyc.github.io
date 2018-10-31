---
layout: post
title:  "Vue-用户管理系统"
date:   2018-07-11 17:06:44
tags: Vue demo bootstrap
color: rgb(255,210,32)
cover: '../assets/vuecustomer.png'
subtitle: '这是一个学习Vue期间做得小demo，连接本地Jsonserver数据库实现了数据的增删改查功能，用的是vue-resource请求数据'
---
## 最初的想法
在学习Vue的时候，就想着做一个demo来做简单的用户管理，实现CURD的所有操作，因为Node.js还学的不够扎实，就想着先用本地数据库来做，就用到了Jsonserver来搭建

### 界面部分

#### 主页界面
![](http://phcdkzm5f.bkt.clouddn.com/vuecustomer.png)

主页界面中的search是利用ES6自带的filter方法对数据库进行筛选，一个难点，想了很多办法，最后还是根据一些博客，采用了filter

```javascript
filterBy(customer,value){
  return customer.filter((customer)=>{
    return customer.name.match(value);
  });
}
```

#### 添加用户界面
![](http://phcdkzm5f.bkt.clouddn.com/customer1.png)

用bootstrap框架搭建的界面，整体界面上比较简洁，主要是为了实现功能

#### 详情页面

![](http://phcdkzm5f.bkt.clouddn.com/customer3.png)

这个页面就是来实现查询，修改以及删除的功能，根据生产的id在数据库内查询当前点击的内容，在点击编辑时同样通过id获取内容，填充表格，修改提交至数据库，删除亦然

这是我对一个小项目的总结，欢迎大家指点，也欢迎大家访问我的[github](https://github.com/onlyhyc)

---
