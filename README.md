## 1.安装开发环境
#### vs code https://code.visualstudio.com 
```
开发时所用的编辑器，内置了终端，开发时使它执行命令运行程序
```
#### Node.js https://nodejs.org 
```
JS服务器端的运行环境，内置npm包管理器，管理项目依赖的各种模块，编译代码，自动部署到服务器就全靠他了
设置npm淘宝镜像
npm config set registry https://registry.npm.taobao.org 
npm config list #查看npm当前配置
```

### 2.安装全局模块
#### webpack
```
npm install -g webpack
```
webpack是一款模块加载器兼打包工具，它能把各种资源，例如JS（含JSX）、coffee、样式（含less/sass）、图片等都作为模块来使用和处理


### 3. 安装vue脚手架
```
npm install vue-cli -g
```

### 4. 在硬盘上找一个文件夹放工程用的，在终端中进入该目录
```
cd 目录路径
```

### 4.根据模板创建项目
```
vue init webpack-simple 工程名字<工程名字不能用中文>

或者创建 vue1.0 的项目

vue init webpack-simple#1.0 工程名字<工程名字不能用中文>

会有一些初始化的设置，如下输入:

Target directory exists. Continue? (Y/n) 直接回车默认(然后会下载 vue2.0模板，这里可能需要连代理)

Project name (vue-test) 直接回车默认

Project description (A Vue.js project) 直接回车默认

Author 写你自己的名字
```

### 5. cd 命令进入创建的工程目录
```
    cd 项目目录
```

## 6. 工程目录结构
```
src：项目源码。开发的时候代码写在这里。
 |--assets # 项目静态资源，编译时不进行处理的资源都放这里
 |--components # 项目公共组件库
 |--config # 公共配置文件，例如路由配置等
 |--css # 项目公共样式库
 |--modules # 项目应用模块，根据应用需要，还可以有子模块，各子模块目录结构和顶级子模块类似
 |    |--components # 模块级公共组件
 |    |--views # 模块视图
 |    |--css # 模块样式
 |    |--js # 模块脚本
 |--App.vue # 项目根视图
 |--main.js # 项目入口文件
 |--store # 基于vuex的状态管理模块
 |    |--index.js # 入口及store初始化
 |    |--event-name.js # mutation名称定义
 |    |--state.js # 根state
 |    |--mutations.js # 根mutation
 |    |--getters.js # 根getter
 |    |--actions.js # 根action
 |    |--modules # 子模块的store对象
 |    |    |--menu.js # menu模块
 |--apis # 服务层ajax请求服务
 |    |--mock # api数据mock服务
 |--utils # 公共库函数
 ```



### 7. 安装项目依赖
```
一定要从官方仓库安装，npm 服务器在国外所以这一步安装速度会很慢。

npm install

不要从国内镜像cnpm安装(会导致后面缺了很多依赖库)

cnpm install
```

### 8. 安装 vue 路由模块 vue-router 和网络请求模块 vue-resource
```
cnpm install vue-router vue-resource --save
```

### 9. 启动项目
```
npm run dev
```

### 10. 填坑(以下坑可能由于 vue2.0 导致其他相关编译打包工具没更新导致的)
```
【重点】后来发现这些坑是由于 npm 不是最新的版本3.10.2， 用 npm 3.9.5就会出现以下坑

解决办法: 请运行以下命令

npm update -g
```

