# vue-bnhcp <img src="https://img.shields.io/badge/bnhcp-v1.0.0-green.svg"/>

> Node.js(v6.9.1) + express(4.X) + vue(2.0) + vuex + mysql(5.7.18) + （NUXT）SSR + nginx反向代理
## 前言 <img src="https://img.shields.io/badge/preface-v1.0.0-yellowgreen.svg"/>

*本项目纯属个人练习项目，数据并非真实，如有雷同，纯属巧合。

本项目是公司项目，公司的技术实现是 cakephp php的mvc框架，由于cakephp view 模板ctp 和 html写在同一
文件，前端部分（view）页面惨不忍睹，难维护，效率低，沟通成本大，迫于无奈，奔着君子动手不动口的原则（所有的技术不是口头上的，需要自己动手，踩坑，你才可以成长），闲暇之余 利用 vue + srr + node + mysql nginx代理 重构本项目，这样既加强了对vue的学习认知，也很好的把vue和node结合，对于数据库的选型，mysql，比较稳定，更通用，老牌值得信赖 ～～由于时间并不充裕，功能实现可能的并不完美，我尽力按需求文档实现～～～现在的页面大概有20个左右，涉及注册、登录、课程列表、课程详情、购物车、提交订单、个人中心等等，最终完成应该会有50个页面左右～需要时间啊...

项目持续进行中~

NUXT 能为我们做什么

问题1：就是我们无需为了路由划分而烦恼，你只需要按照对应的文件夹层级创建 .vue 文件就行

问题2：无需考虑数据传输问题，nuxt 会在模板输出之前异步请求数据（需要引入 axios 库），而且对 vuex 有进一步的封装

问题3：内置了 webpack，省去了配置 webpack 的步骤，nuxt 会根据配置打包对应的文件

还有很多便捷之处，可以尝试去写一写，读读源码

## 项目截图 <img src="https://img.shields.io/badge/build-v1.0.0-blue.svg"/>

<img src="https://github.com/github1586/bnhcp/blob/master/static/img/show1_gif.jpg" width="280"/>


![avatar](https://github.com/github1586/bnhcp/blob/master/static/img/show4_gif.gif)
![avatar](https://github.com/github1586/bnhcp/blob/master/static/img/show5_gif.gif)

![avatar](https://github.com/github1586/bnhcp/blob/master/static/img/show6_gif.gif)
![avatar](https://github.com/github1586/bnhcp/blob/master/static/img/show7_gif.gif) 

![avatar](https://github.com/github1586/bnhcp/blob/master/static/img/show2_gif.gif)
![avatar](https://github.com/github1586/bnhcp/blob/master/static/img/show3_gif.gif)

## 感谢～ <img src="https://img.shields.io/thank/you-v1.0.0-ff69b4.svg"/>

如果我的项目对您有所帮助，您可以点右上角 "Star" 支持一下 感谢～～！

git clone 项目地址 进入 local文件夹 cd template 里面是本地（node）写死的数据可以 

然后 --  yarn install 和 npm run dev

另一种 也可以找我 拿sql文件，自己跑本地服务

线上项目地址：<a href="http://bnhcp.pboss.cc" target="_blank" style="color: red;">bnhcp.pboss.cc</a>  （Google Chrome观看更佳）

扫码 进入 项目

![avatar](https://github.com/github1586/bnhcp/blob/master/static/img/myproject.png)

有疑问或者项目有什么问题 可以联系企鹅 995189950 微信搜索：node-s 或者 Issues me

欢迎大家来给我提提意见 互相探讨~

## 部署 <img src="https://img.shields.io/project/deploy-v1.0.0-blue.svg"/>

阿里云ECS服务器 centos7 

0、安装配置 nvm（node） mysql nginx（Tengine）

1、下载xftp 连接自己服务器，把自己的项目丢进去。

2、cd myproject

3、yarn install（npm install）

4、配置数据库配置文件

5、配置nginx 文件 进行代理 代理所有80端口

6、npm run dev

7、npm run build

8、上面忘记安装pm2， yarn add pm2 （开启 node server 使用）

9、pm2 start build/mian.js

10、查看 pm2 list 列表，查看启动状态

11、pm2 monit  监视所有进程

12、开启 ./nginx

13、如果一切正常，但是访问不通，可以pm2 logs 查看是否报错？

## 完成功能 <img src="https://img.shields.io/badge/complete-v1.0.0-origin.svg"/>

1. 首页渲染
2. 课程的分类搜索
3. 课程 按 （智能排序 价格最高 价格最低 老师好评 人气最高） 排序
4. 课程 按 （班级类型 活动优惠 上课时间（周一到周日） 具体时间（上午下午晚上） 价格区间） 筛选
5. 完成课程列表的下拉加载更多 
6. 课程详情
7. 预约试听 
8. 分类页面
9. 我的页面
10. 提交订单
11. 登录（注册暂无）
12. 阿里云部署

## 预计功能 <img src="https://img.shields.io/badge/estimate-v1.0.0-ff69b4.svg"/>
1. 购物车 （尚未完整）
2. 头像上传
3. 家长添加孩子
4. 报名
5. 优惠券
6. 我的订单
7. 机器人客服
8. redis 首页缓存
（有些页面没有在此处写，根据项目进度往上加~）
## 个人 <img src="https://img.shields.io/oneself/my-ff69b4.svg"/>

爱生活 爱技术 爱折腾

## Build Setup <img src="https://img.shields.io/badge/build-v1.0.0-blue.svg"/>

``` bash
# install dependencies
$ npm install  or yarn install

# serve with hot reload at localhost:3000
$ npm run dev



