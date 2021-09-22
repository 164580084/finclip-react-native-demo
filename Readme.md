<p align="center">
    <a href="https://www.finclip.com?from=github">
    <img width="auto" src="https://www.finclip.com/mop/document/images/logo.png">
    </a>
</p>

<p align="center"> 
    <strong>FinClip ReactNative DEMO</strong></br>
<p>
<p align="center"> 
        本项目提供在 ReactNative 环境中运行小程序的 DEMO 样例
<p>

<p align="center"> 
	👉 <a href="https://www.finclip.com?from=github">https://www.finclip.com/</a> 👈
</p>

-----
## 🤔 FinClip 是什么?

有没有**想过**，开发好的微信小程序能放在自己的 APP 里直接运行，只需要开发一次小程序，就能在不同的应用中打开它，是不是很不可思议？

有没有**试过**，在自己的 APP 中引入一个 SDK ，应用中不仅可以打开小程序，还能自定义小程序接口，修改小程序样式，是不是觉得更不可思议？

这就是 FinClip ，就是有这么多不可思议！

## 🤩 效果预览

**本项目是 FinClip 小程序在 ReactNative 工程基础上下集成及运行小程序 DEMO 演示，您可以按照下方流程测试，验证 FinClip 小程序在 ReactNative 环境下的实际效果。**

先看一下运行效果~

<p align="center">
    <a href="#">
    <img width="auto" src="./docs/mop-react-native-demo.gif">
    </a>
</p>

## ⚙️ 操作步骤
### 第一步 引入小程序引擎插件
在 `package.json` 文件中引入小程序 ReactNative 插件

`"react-native-mopsdk": "^1.0.1"`

### 第二步 初始化引擎
在 `main.dart` 文件中增加以下小程序引擎初始化方法。

在 Mop.instance.initialize 中，需要用到 `SDK KEY` 和 `SECRET`。

```objc
import MopSDK from 'react-native-mopsdk';
// 1. mop初始化
MopSDK.initialize({
    appkey: '22LyZEib0gLTQdU3MUauASlb4KFRNRajt4RmY6UDSucA',
    secret: '4a915e447bcbd439',
    apiServer: 'https://api.finclip.com',
    apiPrefix: '/api/v1/mop'
  }, (data) => {
    console.log('message;', data);
  });
```

### 第三步 打开小程序
```objc
MopSDK.openApplet('appid','','',(data)=>{});
```

- **SDK KEY** 和 **SDK SECRET** 可以从 [FinClip](https://finclip.com/#/home)  获取，点 [这里](https://finclip.com/#/register) 注册账号；
- 进入平台后，在「应用管理」页面添加你自己的包名后，点击「复制」即可获得  key\secret\apisever 字段；
- **apiServer** 和 **apiPrefix** 是固定字段，请直接参考本 DEMO ；
- **小程序 ID** 是管理后台上架的小程序 APP ID，需要在「小程序管理」中创建并在「应用管理」中关联；
> 小程序 ID 与 微信小程序ID 不一样哦！（这里是特指 FinClip 平台的 ID ）


## 📋 接口文档
[点击这里](https://www.finclip.com/mop/document/introduce/quickStart/intergration-guide.html#_4-reactnative-%E5%BF%AB%E9%80%9F%E9%9B%86%E6%88%90) 查看 React Native 快速集成文档

## 🔗 常用链接
以下内容是您在 FinClip 进行开发与体验时，常见的问题与指引信息

- [FinClip 官网](https://www.finclip.com/#/home)
- [示例小程序](https://www.finclip.com/#/market)
- [文档中心](https://www.finclip.com/mop/document/)
- [SDK 部署指南](https://www.finclip.com/mop/document/introduce/quickStart/intergration-guide.html)
- [小程序代码结构](https://www.finclip.com/mop/document/develop/guide/structure.html)
- [iOS 集成指引](https://www.finclip.com/mop/document/runtime-sdk/ios/ios-integrate.html)
- [Android 集成指引](https://www.finclip.com/mop/document/runtime-sdk/android/android-integrate.html)
- [Flutter 集成指引](https://www.finclip.com/mop/document/runtime-sdk/flutter/flutter-integrate.html)

## ☎️ 联系我们
微信扫描下面二维码，关注官方公众号 **「凡泰极客」**，获取更多精彩内容。<br>
<img width="150px" src="https://www.finclip.com/mop/document/images/ic_qr.svg">

微信扫描下面二维码，邀请进官方微信交流群（加好友备注：finclip 咨询），获取更多精彩内容。<br>
<img width="150px" src="https://finclip-homeweb-1251849568.cos.ap-guangzhou.myqcloud.com/images/ldy111.jpg">

## Stargazers
[![Stargazers repo roster for @finogeeks/finclip-react-native-demo](https://reporoster.com/stars/finogeeks/finclip-react-native-demo)](https://github.com/finogeeks/finclip-react-native-demo/stargazers)

## Forkers
[![Forkers repo roster for @finogeeks/finclip-react-native-demo](https://reporoster.com/forks/finogeeks/finclip-react-native-demo)](https://github.com/finogeeks/finclip-react-native-demo/network/members)
