# telegraph-Image


### [Demo](https://img.131213.xyz/)

### 开发计划
- [x] 后台管理
- [x] 鉴黄
- [ ] 画廊

### 优点

1. 无限图片储存数量，你可以上传不限数量的图片

2. 无需购买服务器，托管于Cloudflare的网络上，当使用量不超过Cloudflare的免费额度时，完全免费

3. 无需购买域名，可以使用Cloudflare Pages提供的*.pages.dev的免费二级域名，同时也支持绑定自定义域名

4. 支持图片审查API，可根据需要开启，开启后不良图片将自动屏蔽，不再加载

5. 支持后台图片管理，日志管理，可以对上传的图片进行在线预览，添加白名单，黑名单等操作



### 利用Cloudflare pages部署

1. 点击[Use this template](https://github.com/x-dr/telegraph-Image/generate)按钮创建一个新的代码库。

2. 登录到[Cloudflare](https://dash.cloudflare.com/)控制台.
3. 在帐户主页中，选择`pages`> ` Create a project` > `Connect to Git`
4. 选择你创建的项目存储库，在`Set up builds and deployments`部分中，全部默认即可。

<img src="https://i3.wp.com/telegra.ph/file/beb0385822e24c9a9d459.png" />

5. 点击`Save and Deploy`部署，然后点`Continue to project`即可看到访问域名

#### 后台管理不是很完善 但基本的应该都有了 

**[开启图片管理功能教程](./docs/manage.md)**

---
### 利用vercel部署(vercel分支)

[![Deploy with Vercel](https://vercel.com/button?utm_source=busiyi&utm_campaign=oss)](https://vercel.com/new/clone?utm_source=busiyi&utm_campaign=oss&repository-url=https://github.com/x-dr/telegraph-Image/tree/vercel)

---





### 自定义cdn加速
> 默认是使用cloudflare ,修改 `asset/js/upload.js#L219` 即可

+ 如用cachefly加速 

cachefly绑定cloudflare pages
<img src="https://i3.wp.com/telegra.ph/file/c19f7ea17ce2027b13dfa.png" />

修改代码

```diff
- const PROXYURL = ""  //自定义加速域名 默认是使用cloudflare
+ const PROXYURL = "https://xxxxxxxxxx.cachefly.net"  //自定义加速域名 默认是使用cloudflare
```




### 感谢

[@cf-pages](https://github.com/cf-pages/Telegraph-Image)

[@likebeta](https://github.com/likebeta/telegraph-image-hosting)




