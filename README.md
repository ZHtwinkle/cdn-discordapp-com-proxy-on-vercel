# 使用 Vercel 反代 cdn.discordapp.com 

- [使用 Vercel 反代 cdn.discordapp.com ](#使用-vercel-反代-cdn.discordapp.com-教程)
  - [简介](#简介)
  - [使用](#使用)
  - [要求](#要求)
  - [部署](#部署)

## 简介

国内只是墙了 vercel 本身的域名，但是自定义域名没有墙，因此做了代理并绑定域名之后就可以用自己的域名在国内直连 cdn.discordapp.com 了。
理论上也可以代理其他被墙的站点。
## 使用方法

- 访问 cdn.discordapp.com 时，将 "cdn.discordapp.com" 换成你的自定义域名，例如

## 要求

- 一个域名（无需备案），没有的话可以在阿里云或者腾讯云上买一个几块钱一年的


## 部署

1. 点击一键部署按钮

   [![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https%3A%2F%2Fgithub.com%2FZHtwinkle%2Fcdn-discordapp-com-proxy-on-vercel&project-name=cdn-discordapp-com-proxy-on-vercel&repository-name=cdn-discordapp-com-proxy-on-vercel&root-directory=src)

2. 用 Github 登录 Vercel，没有 Github 账户的去注册一个，网上很多教程就不展开了

3. 登录之后点击 Create 按钮

4. 接着等十几秒钟就创建好项目了，接下来进入仪表盘

5. 进入到项目里之后，依次点击 Settings -> Domains，然后添加你的域名。添加的域名类型有两种，一种是一级域名(xxxx.com)和二级域名(openai.xxxx.com)，我个人推荐使用二级域名，因为一级域名一般用来做网站展示用，只能有一个，而二级域名可以有无限个（只要你有一个域名就可以自己创建无限个二级域名）

6. 添加域名有三种方式，这里我们选第三种，因为简单

7. 接下来会分两种情况，分为一级域名和二级域名，都有教程，以阿里云为例（其他厂商也是差不多的配置，很简单的）

   1. 一级域名

      添加一级域名后 Vercel 会提示让你添加 DNS 解析记录

      在域名解析的解析设置里点击 添加记录，按照 Vercel 的提示配置好图中三个选项，点击确认

      回 Vercel 点击 Refresh 按钮，出现下图所示的情况就表明配置完成了

   2. 二级域名（以 openai 主机记录为例，可以改成自己喜欢的）

      添加二级域名后 Vercel 会提示让你添加 DNS 解析记录

      在阿里云域名解析的解析设置里点击 添加记录，按照 Vercel 的提示配置好图中三个选项，点击确认

      回 Vercel 点击 Refresh 按钮，出现下图所示的情况就表明配置完成了

