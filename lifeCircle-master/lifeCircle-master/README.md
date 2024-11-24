# 校园生活圈小程序

拥有 表白墙、失物招领、兼职、闲置物品等功能

## 基于云开发（参考文档）

- [云开发文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/basis/getting-started.html)

## 部署教程

1. 将该项目导入微信开发者工具
2. 更改 miniprogram/app.js 里面的云环境id

```bash
wx.cloud.init({
	env:'xxx',  //xxx为你的云环境id
    traceUser: true
})
```

3. 创建对应的五个数据库集合（biaobai、found、lost、xianzhi、jianzhi）
4. 将 cloudfunctions 文件下的四个文件上传云函数部署（右键点击，选择第三个选项“上传并部署：云端安装环境”）

## 数据库及字段名

表白墙（biaobai）

| 字段名     | 类型   | 用处             |
| ---------- | ------ | ---------------- |
| _id        | string | 数据id，默认生成 |
| _openid    | string | 用户openid       |
| createTime | date   | 数据生成时间     |
| sendTIme   | string | 数据发送时间     |
| info       | string | 表白信息         |
| to         | string | 表白对象         |
| writer     | string | 发送者           |

拾物和失物（found lost）

| 字段名     | 类型   | 用处             |
| ---------- | ------ | ---------------- |
| _id        | string | 数据id，默认生成 |
| _openid    | string | 用户openid       |
| createTime | date   | 数据生成时间     |
| sendTIme   | string | 数据发送时间     |
| fileIDs    | Array  | 图片地址         |
| info       | string | 文字信息         |
| name       | string | 物品名称         |
| userName   | string | 用户名称         |
| touxiang   | string | 用户头像         |
| pCall      | string | 电话             |
| pWechat    | string | 微信             |

兼职（jianzhi）

| 字段名  | 类型   | 用处             |
| ------- | ------ | ---------------- |
| _id     | string | 数据id，默认生成 |
| _openid | string | 用户openid       |
| time    | date   | 数据生成时间     |
| call    | string | 联系电话         |
| daiyu   | string | 待遇             |
| didian  | string | 地点             |
| gangwei | string | 岗位             |
| gongsi  | string | 公司             |
| neirong | string | 工作内容         |
| shijian | string | 工作时间         |
| writer  | string | 猎头             |
| yaoqiu  | string | 要求             |

## 如果对您有用，欢迎支持作者，谢谢

<img src="http://rose-ccc.gitee.io/imgbed/pay/alipay.png" width = "150px" align=“center”></img>
<img src="http://rose-ccc.gitee.io/imgbed/pay/wechatpay.png" width = "150px" align=“center”></img>

## 程序截图

### 首页

<img src="http://rose-ccc.gitee.io/imgbed/%E6%A0%A1%E5%9B%AD%E7%94%9F%E6%B4%BB%E5%B0%8F%E7%A8%8B%E5%BA%8F/index.png" width = "108px" height = "234px" align=“center”></img>
### 我的
<img src="http://rose-ccc.gitee.io/imgbed/%E6%A0%A1%E5%9B%AD%E7%94%9F%E6%B4%BB%E5%B0%8F%E7%A8%8B%E5%BA%8F/mine.png" width = "108px" height = "234px" align=“center”></img>
### 表白墙
<img src="http://rose-ccc.gitee.io/imgbed/%E6%A0%A1%E5%9B%AD%E7%94%9F%E6%B4%BB%E5%B0%8F%E7%A8%8B%E5%BA%8F/love.png" width = "108px" height = "234px" align=“center”></img>
### 失物招领
<img src="http://rose-ccc.gitee.io/imgbed/%E6%A0%A1%E5%9B%AD%E7%94%9F%E6%B4%BB%E5%B0%8F%E7%A8%8B%E5%BA%8F/lost.png" width = "108px" height = "234px" align=“center”></img>
<img src="http://rose-ccc.gitee.io/imgbed/%E6%A0%A1%E5%9B%AD%E7%94%9F%E6%B4%BB%E5%B0%8F%E7%A8%8B%E5%BA%8F/lostSend.png" width = "108px" height = "234px" align=“center”></img>
### 兼职
<img src="http://rose-ccc.gitee.io/imgbed/%E6%A0%A1%E5%9B%AD%E7%94%9F%E6%B4%BB%E5%B0%8F%E7%A8%8B%E5%BA%8F/work.png" width = "108px" height = "234px" align=“center”></img>
<img src="http://rose-ccc.gitee.io/imgbed/%E6%A0%A1%E5%9B%AD%E7%94%9F%E6%B4%BB%E5%B0%8F%E7%A8%8B%E5%BA%8F/workDetail.png" width = "108px" height = "234px" align=“center”></img>
### 闲置
<img src="http://rose-ccc.gitee.io/imgbed/%E6%A0%A1%E5%9B%AD%E7%94%9F%E6%B4%BB%E5%B0%8F%E7%A8%8B%E5%BA%8F/buy.png" width = "108px" height = "234px" align=“center” />
<img src="http://rose-ccc.gitee.io/imgbed/%E6%A0%A1%E5%9B%AD%E7%94%9F%E6%B4%BB%E5%B0%8F%E7%A8%8B%E5%BA%8F/buySend.png" width = "108px" height = "234px" align=“center” />
<img src="http://rose-ccc.gitee.io/imgbed/%E6%A0%A1%E5%9B%AD%E7%94%9F%E6%B4%BB%E5%B0%8F%E7%A8%8B%E5%BA%8F/buyDetail.png" width = "108px" height = "234px" align=“center” />

## 最后（更改于2023-12）

因为这是个大二期间做的项目，没想到有这么多star，很感谢大家的支持，很多私聊回不过来了，大家好像都不提issue，gitee也关闭了评论

所以建立个QQ群，大家可以群里讨论遇到的问题，相信大家以这个项目作为前端学习的入门，一定会有所收获

“热爱技术，热爱生活！”

![输入图片说明](WechatIMG95.jpg)
