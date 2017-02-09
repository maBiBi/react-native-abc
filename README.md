atom 快捷键
control command 上下  = 整行替换移动
tab 多行右移
shift tab  多行左移


8-13
A5纸边靠门口
输出PDF 再打印,打印机首选项选择双面

8-30
windows版本 react-native init 无反应要装git

'android-23' android studio 缺23sdk

8-31
flex是弹性盒子布局,由伸缩容器container和伸缩项目item组成

9-2
网络图片 source={{uri:'http://.png'}}
本地图片 source={require('./.png')}
render=渲染

12-9
mongoDb
mongo
show dbs 显示数据库
use xxx  选择数据库
show tables 显示表
db.xxx.remove({}) 删除所有表
db.dropDatabase() 删除整个数据库!慎用
db.xxx.insert({}) 插入数据
查询数据
db.xxx.find().skip(3).limit(2).sort({}x:1)
find寻找  skip跳过  limit限制数量 sort排序

更新数据
db.xxx.update({x:1},{x:999})   //X:1,更新成x:999

12-14
用你喜欢的编辑器创建一个 helloWorld.js文件：
var http = require('http'); 
 
http.createServer(function(req,res){ 
        res.writeHead(200, { 'Content-Type': 'text/plain' });  
        res.end('Hello world!'); 
}).listen(3000); 
 
console.log('Server started on localhost:3000; press Ctrl-C to terminate....');

12-19 <4章2> ES5升级ES6
var React = require('react-native')
import React from 'react-native'

var width = Dimensions.get('window').width
const width = Dimensions.get('window').width

var imoocApp = React.createClass({
  getInitialState(){
    return {
     user: null,
     selectedTab: 'list'
   }
 }
})
class imoocApp extends Component {
  constructor(props){
    super(props)
    
    this.state = {
      user: null,
      selectedTab: 'list'
  }
 }
}

<Account user={this.state.user} logout={this._loggout} />
<Account user={this.state.user} logout={this._loggout.bind(this)} /> 需要绑定this

var Edit = React.createClass({
  getInitialState(){
   
 }
})

export default class Edit extends Component {
  constructor(props){
    super(props)
 }
}

ActivityIndicatorIOS被弃用
animated Modal被弃用  
<Modal animated={'slide'} />
<Modal animationType={'slide'} />

var React = require('react-native');
var { AppRegistry } = React;
var WeatherProject = require('./WeatherProject');
AppRegistry.registerComponent('WeatherProject', () => WeatherProject);

//改成,2.5版本后更新的

import React, { Component } from 'react';import {    StyleSheet,    Text,    View,    TextInput,    Image} from 'react-native';

10-10
安装sublime编辑器,安装packgeControl语法高亮包.
进入packgeControl.io>点 install now,复制代码.
sublime 按 control + ~ , 粘贴代码>回车
装完后> 按 command + shift + P > install > 回车 输入babel>安装,
按 command + shift + P > install > 回车>输入sublimelinter-jsxhint  安装
再装gitgutter,sublimelinter,sublimelinter-contrib-es
安装语法错误提示
nam install -g aslant babel-eslint —registry=http://registry.npm.taobao.org

项目文件说明:
package.json  项目配置文件,组件版本
node.modules/  依赖模块
index.ios.js   IOS平台入口
.flowcofig     js代码检查设定
.gitignore      设置那些代码上传github
.watchmanconfig   语法检查 


引入 tabBarIOS,
安装icon库 (图标)  npm i react-native-vector-icons@2.02 —save
安装rnpm(把模块引入到工程)   npm i rnpm@1.7.0 -g
版本号  react-native -v (查看cli脚手架版本)
链接icon库到项目   rnpm link react-native-vector-icons
?? link不到icons  //升级rpm   npm i -g rpm to update (或安装时不指定版本 去掉@1.7.0)
10-12
使用特定版本创建工程
react-native init  [Project Name] —source react-native@0.22.2

ioncions 引入(ES6) import Icon from 'react-native-vector-icons/Ionicons';     <Icon.TabBarItem>
组件成功导入,即使icon名错误 会有?出

10-14
onEndReached  触底加载
onEndReachedThreshold  触底前多少加载

10-17
错误 cannot read property ‘Constans’ of undefined    导入video组件 要重新运行项目

.toFixed(2)  保留两位小数

10-18   (课程5-17)
Button 要用import引入  var会报错

10-19
jsCodeLocation

10-21
安装 react-native-image-picker,
reacct-native link react-native-image-picker

10-22
8~6 npm i react-native-progress —save

10-24
/user/用户名/Caches/Homebrew 

mongoldb 错误61,重启 sudo mongo

10-25
npm i koa koa-logger koa-session koa-bodyparser koa-bodyparser koa-router mongoose sha1 lodash
uuid xss bluebird speakeasy —save
      koa   
	  koa-logger 开发环境下的日志中间件,
	  koa-session 基础cookie会话中间件,保持用户会话状态
  	    koa-bodyparser  解析表单数据等等来生成对象结构数据的中间件
 	    koa-router   路由中间件,为不同的url地址分配不同的规则
	    mongoose    数据库的对象建模工具
	    sha1             哈希算法库,加密一些数据
 	    lodash            js编程的瑞士刀,提供许多好用的工具函数
	    uuid             生成以为不会重复的ID
	    xss              对用户输入内容进行过滤,避免xss恶意攻击的模块
	    bluebird       等于promise标准实现封装后的promise库
	    speakeasy	生成随机数字的工具库
	    	
10-26
chrome浏览器 开发者模式 安装 DHC REST Client 调试工具
trim() 去掉前后空格

10-27
SyntaxError: Unexpected token N in JSON at position 0  解析不到JSON
签名的路径不对

最后一个属性不能有逗号

index.ios.js 里 selectedTab 设置启动停留界面

11-26
选择视频后报错,Video组件引入的方式不对.应该是var Video = require('react-native-video').default

11-30
服务器没反应,检查config里api的ip

12-1
TypeError: qiniu.rs.PutPolicy2 is not a constructor    服务端app没有引入nam install qiniu

12-2
Unhandled rejection (<{"error":{"message":"Error in loading ...>, no stack trace)
Promise catch错误代码没有写

12-3
11.8 Cannot read property   答: rpm后需要重建项目

12-5
上传wloudinary失败 
{"error":{"message":"Invalid Signature 99612dd51df596abee51bea4746984b7dde3b97f. String to sign - 'folder=audio&tags=app, audio&timestamp=1480906834786'."}}
原因: edit.js  var tags = 'app, audio' 里多了空格

注意路径的 ‘/’

12-15
安装Robomongo  数据库可视化工具

12-16
nam i -g supervisor  改服务端代码后自动重启
supervisor --harmony app

12-18 第二遍
<2章1>
OSX更新到最新,
安装最新xcode,
appStore下载

安装homebrew: 包管理工具,
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

安装watchman: facebook的开源项目,监视文件并记录改动情况
安装flow: javaScritp的静态类检查器,用于找出JavaScript代码的类型错误
brew install watchman flow git gcc pig-config cairo libpng jpeg gitlab mongodb

安装nvm: 包管理仓库
curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.32.1/install.sh | bash

安装node.js
—

安装淘宝源 全局
sudo npm install cnpm -g

安装react-native

老师安装了命令行工具iterm2 可选

<2章2>
安装RN脚手架
cnpm install -g react-native-cli

创建一个RN项目
react-native init abc

启动项目
cd abc
react-native run-ios

12-23 rnpm link
npm i rnpm -g
rnpm link react-native-vector-icons

12-24
image-pick 要rnpm link

12-27
onPress={this._create}  和 onPress={this._create()} 不一样,后者会启动功能块
nam i react-native-maps —save
rnpm link react-native-maps  安装地图组件

12-28 maps
style={{height: 200, margin: 40}}  要声明大小,不然白屏

12-30
变量后面不能有逗号

12-31 mock.js
nam i mocks —save

箭头函数
var newberArray = [2,3,5,6]
var newNumberArray = numberArray.map(function(item){
	return item + 1
}
等效于
var newNumberArray = numberArray.map(item => item + 1)

1-1 flex-direction
row 水平左往右, row-reverse 水平右往左
column 垂直上到下, column-reverse 垂直下到上

对齐左右边要用position
position: 'absolute',right: 5

获取数据 mock是把获取来的简单json变成随机数据
_fetchData: function (){
  fetch('http://rap.taobao.org/mockjs/12433/api/creations?accessToken=123')
    .then((response) => response.json())
    .then((response) => {
      var data = Mock.mock(response)
      if (data.success) {
        this.setState({
          dataSource: this.state.dataSource.cloneWithRows(data.data)
        })
      }
      console.log(data);
    })
    .catch((error) => {
      console.warn(error)
    });
},

1-2 .和..
../common/request 表示上一层目录
./request 表示同一层目录

ListView row style加入flex: 1 会白屏

1-5 react-native-sk-countdown
import {CountDownText} from 'react-native-sk-countdown'
安装react-addons-update,到 node_modules 下找到 react-native-sk-countdown 下的 CountDownText.js 改成
import React,{Component} from 'react' 
import { StyleSheet, Text, } from 'react-native';
var update = require('react-addons-update') 
var countDown = require('./countDown')

卸载模块 nam uninstall 模块 —save


  <Text style={styles.avatarTip}>重新上传身份证</Text>
            </Image>
          </TouchableOpacity>
            : <View style={styles.toolbar}>
                <Text style={styles.toolbarTitle}>验证</Text>
                <Text style={styles.toolbarExtra} onPress={this._edit}>编辑</Text>
              </View>
      //    <TouchableOpacity onPress={this._pickPhoto} style={styles.avatarContainer}>
          <Text style={styles.avatarTip}>请上传身份证正面,通过验证后系统将按个人资料匹配待遇更好的工作.</Text>
          <Text style={styles.avatarTip}>该图片验证后将在服务器上删除,以保障个人资料安全</Text>

          <View style={styles.avatarBox}>

          <View style={styles.fieldItem}>
                   <Text style={styles.label}>昵称</Text>
                   <TextInput
                      placeholder={'输入你的昵称'}
                      style={styles.inputField}
                      autoCapitalize={'none'}
                      autoCorrect={false}
                      defaultValue={user.nickname}
                      onChangeText={(text) => {
                        this._changeUserState('nickname', text)
                      }} />
                </View>

2-7
react-native-image-picker 要rnpm
rnpm link react-native-image-picker
点相册 闪退,用Xcode打开项目> info里添加 相册描述 NSPhotoLibraryUsageDescription

	?	NSContactsUsageDescription -> 通讯录
	?	NSMicrophoneUsageDescription -> 麦克风
	?	NSPhotoLibraryUsageDescription -> 相册
	?	NSCameraUsageDescription -> 相机
	?	NSLocationAlwaysUsageDescription -> 地理位置
	?	NSLocationWhenInUseUsageDescription -> 地理位置
	?	Privacy - Bluetooth Peripheral Usage Description -> 蓝牙权限
	?	Privacy - Speech Recognition Usage Description -> 语音转文字权限
	?	Privacy - Calendars Usage Description -> 日历权限
	?	Privacy - Contacts Usage Description -> 通讯录权限
	
2-9
update 需要accessToken值
