# vue2-hybridapp-haoshiqi

<p align="center">
  <a href="https://circleci.com/gh/vuejs/vue/tree/dev"><img src="https://img.shields.io/circleci/project/vuejs/vue/dev.svg" alt="Build Status"></a>  
  <a href="https://www.npmjs.com/package/vue"><img src="https://img.shields.io/npm/v/vue.svg" alt="Version"></a>
  <a href="https://www.npmjs.com/package/vue"><img src="https://img.shields.io/npm/l/vue.svg" alt="License"></a>
  <br>
</p>

# 说明

>  这个项目是关于 vue2 + vue-router + vuex + cordova + nodejs 的项目实战开发

>  所有的数据通过node request 获取(后台代码详见backend目录)

>  前后端分离的架构设计，配置webpack-dev-server的反向代理实现前后端数据的通信.（前端代码详见haoshiqi目录）

>  结合cordova api实现硬件访问功能，通过phonegap开发者预览工具进行测试(cordova工程详见hybirdApp目录)

>  这个项目有两个输出产物，一个是单页面的webapp,一个是hybridapp

>  如果对您有帮助，您可以点右上角 "Star" 支持一下 谢谢！ ^_^

>  或者您可以 "follow" 一下，我会继续开源项目

>  如有问题请在 Issues 中提，或者您发现问题并有非常好的解决方案，欢迎 PR 👍



# 项目运行（nodejs 6.0+）
``` bash
# 1. git clone git@github.com:liupeijun/vue2-hybridapp-haoshiqi.git

# 2. 进入backend 目录,安装依赖,启动node服务器

cd backend

npm install

npm start

# 3. 进入haoshiqi目录，安装依赖，启动webpack dev server

cd haoshiqi 

cnpm install(******因为使用了sass，为了顺利完成安装，最好使用cnpm install******)

npm run dev  (开发环境)

npm run build 
(发布环境,为了手机能正常访问node服务器，需要手动修改webpack.config.js,URL:'"http://你的ip地址:3000"'  
dist目录会生成在hybridApp\www 文件夹下，当然dist生成路径可以自行修改)

# 4. 如果要生成混合app,进入hybridApp目录,生成android,ios工程， 最后编译

cd hybridApp

cordova platform add android (cordova platform add ios)

cordova build android 

```

# 架构介绍

<img src="https://github.com/liupeijun/vue2-hybridapp-haoshiqi/blob/master/screenshot/kerwin.png" width="100%" />

# 效果演示
<p>
  <img src="https://github.com/liupeijun/vue2-hybridapp-haoshiqi/blob/master/screenshot/1.png" width="200" float="left"/>
  <img src="https://github.com/liupeijun/vue2-hybridapp-haoshiqi/blob/master/screenshot/2.png" width="200" float="left"/>
  <img src="https://github.com/liupeijun/vue2-hybridapp-haoshiqi/blob/master/screenshot/3.png" width="200" float="left"/>
  <img src="https://github.com/liupeijun/vue2-hybridapp-haoshiqi/blob/master/screenshot/4.png" width="200" float="left"/>

</p>

# 待办事项

>  第三方登录
>  购物车支付
>  消息推送

## License

[MIT](http://opensource.org/licenses/MIT)

Copyright (c) 2016-present, Kerwin Liu
