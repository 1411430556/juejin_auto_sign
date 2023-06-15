### 使用说明

+ [视频教程地址](https://www.bilibili.com/video/BV1P14y1D7VK/?share_source=copy_web&vd_source=31524f9f63a123e44354d99dbeae408e)    👈点我🐾

+ 安装依赖

```
npm install
OR
yarn
```

+ 修改`/config.js`下的`cookie`、`aid`、`uuid`以及`PUSH_PLUS_TOKEN`
+ 本地测试

```
node app.js
```

+ 部署华为云函数自动运行

1. > 在稀土掘金登录你自己的账号并进入签到页，打开控制台→网络，搜索pin开头的，载荷里有`aid`和`uuid`，复制这两个；来到代码，`config.js`里，输入对应的参数。接着搜索check开头的，header里会有你的`cookie`，状态码为200的里面有你的`cookie`，复制下来，填入到你的配置里。
2. > 接下来配置pushplus，在他们的官网[pushplus](http://www.pushplus.plus/)登录, 选择上方发送消息 → 一对一消息，这里就会有你的pushplus token，将它复制下来填入配置文件里。最后这个`_signature`可以不写。
3. > 然后进入[华为云官网](https://www.huaweicloud.com/)，搜索函数工作流，函数前100万次/月调用免费。进入函数列表，选择右上角创建函数，删除默认的入口文件。
4. > 将克隆下来的代码压缩，地址我会放评论区。`node_modules`也一并打包压缩，接下来在右边点击上传自压缩包，会自动解压。
5. > 设置函数执行入口为 `index.main_handler`。
6. > 配置触发器，每天上午9.30分自动签到并会在pushplus微信公众号推送签到结果。此时就创建好了，可以测试一下，我这里就以我配置好了的来演示。配置测试事件选空白模板即可，可以看到成功了，因为我今天已经签到过了。

