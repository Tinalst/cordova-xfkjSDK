# ionic+cordova+科大讯飞语音SDK使用教程

> 使用本教程，默认你的设备已经支持Android开发、cordova开发、ionic开发的环境下，即能创建一个可运行并打包的ionic项目或者cordova项目或者原生安卓项目的前提下
## SDK依赖+插件配置
### 获取cordova-plugin-IFlyspeech-master.zip

`这个插件是由cordova结合科大讯飞语音SDK编写的插件，由官方提供，非本人原创`
> 下载链接： [cordova-plugin-IFlyspeech-master.zip](https://github.com/StellaLim/cordova-xfkjSDK/tree/master/cordova-xfkjSDK/cordova-plugin-IFlyspeech-master)
>> 这个链接下文件包含了package.json文件，是本人做过了处理的，原始官方文件不包含，所以下载下来后可以选择性删除，如果不删除下面的<a href="#jump" target="_self">步骤创建package.json文件步骤</a>请忽略
解压后的目录如下：
```
|--src
|--www
|--plugin.xml
|--README.md
```
### 注册创建自己的讯飞应用
[讯飞官网](https://console.xfyun.cn)
进入官网后进行站好注册，注册完成进入控制台
![Github](https://github.com/StellaLim/readme_pic/blob/master/cordova-xfkjSDK/1.png)
创建应用，选择Android类型的项目
![Github](https://github.com/StellaLim/readme_pic/blob/master/cordova-xfkjSDK/2.png)
添加服务
![Github](https://github.com/StellaLim/readme_pic/blob/master/cordova-xfkjSDK/3.png)
下载SDK
![Github](https://github.com/StellaLim/readme_pic/blob/master/cordova-xfkjSDK/4.png)
下载后的SDK压缩包是长这个样子的

![Github](https://github.com/StellaLim/readme_pic/blob/master/cordova-xfkjSDK/5.png)

解压后的目录如下
```
|-- assets
|--libs
|--res
|-sample
|--readme.txt
|--release.txt
```
进入libs目录
![Github](https://github.com/StellaLim/readme_pic/blob/master/cordova-xfkjSDK/7.png)
将libs目录内的所有文件覆盖到cordova-plugin-IFlyspeech-master\src\android\libs下
### APPID的配置
进入cordova-plugin-IFlyspeech-master，打开cordova-plugin-IFlyspeech-master/plugin.xml文件
![Github](https://github.com/StellaLim/readme_pic/blob/master/cordova-xfkjSDK/8.png)
去科大讯飞的后台自己刚刚创建的应用复制APPID，如下
![Github](https://github.com/StellaLim/readme_pic/blob/master/cordova-xfkjSDK/9.png)
替换plugin.xml下的相应APPID为自己应用的APPID
![Github](https://github.com/StellaLim/readme_pic/blob/master/cordova-xfkjSDK/10.png)
进入cordova-plugin-IFlyspeech-master，打开cordova-plugin-IFlyspeech-master/src/android/res/values/string.xml文件
替换string.xml下的相应APPID为自己应用的APPID
![Github](https://github.com/StellaLim/readme_pic/blob/master/cordova-xfkjSDK/12.png)
## 创建工程
#### 创建ionic项目
```
Ionic start kdxf blank
cd kdxf
```
### <div id="jump">为cordova-plugin-IFlyspeech-master创建package.json配置文件</div>
安装plugma
```
npm  install  -g plugman
```
创建package.json文件
`打开命令行CD到cordova-plugin-IFlyspeech-maste文件夹下执行如下命令执行如下命令`
```
Plugman createpackagejson D:\study\ionic\cordova-plugin-IFlyspeech-master // 你自己本地里的插件的路径
```
执行成功后，当前文件夹会多出一个package.json
![Github](https://github.com/StellaLim/readme_pic/blob/master/cordova-xfkjSDK/13.png)
### 为创建的工程添加插件
进入到工程文件夹下，输入命令
```
cordova plugin add D:\study\ionic\cordova-plugin-IFlyspeech-master
```
![Github](https://github.com/StellaLim/readme_pic/blob/master/cordova-xfkjSDK/14.png)
如上，插件加入成功
### 添加安卓平台
```
cordova platfrom add android@6.4.0 // 请务必安装6.4.0版本
```
![Github](https://github.com/StellaLim/readme_pic/blob/master/cordova-xfkjSDK/15.png)
## 代码测试
![Github](https://github.com/StellaLim/readme_pic/blob/master/cordova-xfkjSDK/16.png)

## 运行效果
![Github](https://github.com/StellaLim/readme_pic/blob/master/cordova-xfkjSDK/17.png)
![Github](https://github.com/StellaLim/readme_pic/blob/master/cordova-xfkjSDK/18.png)

`如有疑问，针对本教程，欢迎提问交流`


