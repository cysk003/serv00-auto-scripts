<div align="right">
   <strong>中文</strong> | <a href="README.md">English</a>
</div>

<img src="https://www.serv00.com/wp-content/themes/serv00/public/svg/logo.svg" alt="serv00 logo" width="50" height="50" align="right" />

<div align="center">

<h1> Serv00/CT8 - Free Host Auto Renewal </h1>

<p>Serv00/CT8 - 免费主机自动续期</p>

</div>

<hr/>

<div align="center">
<a href="https://www.serv00.com/sign-in/">Serv00 登录</a> | 
<a href="https://docs.serv00.com/">serv00 文档</a> | 
<a href="https://forum.serv00.com/">serv00 社区</a>
<a href="https://panel.ct8.pl/">CT8 登录</a> | 
<a href="https://pomoc.mydevil.net/">CT8 文档</a> | 
<a href="https://forum.ct8.pl/">CT8 社区</a>
</div>

<hr/>

## 使用方法

1. 在 GitHub 仓库中，进入右上角`Settings`

2. 在侧边栏找到`Secrets and variables`，点击展开选择`Actions`，点击`New repository secret`
    
3. 然后[创建](https://lopinx.github.io/mydevil/)一个名为`ACCOUNTS_JSON`的`Secret`，将 JSON 格式的账号密码字符串作为它的值，如下格式：  

``` json
[  
  { "username": "qishihuang", "password": "zhanghao", "panel": "panel3.serv00.com" },  
  { "username": "zhaogao", "password": "daqinzhonggong", "panel": "panel1.serv00.com" },  
  { "username": "heiheihei", "password": "shaibopengke", "panel": "panel.ct8.pl" }  
]
```

> 其中`panel`参数为面板域名，即为你所收到注册邮件的`panel*.serv00.com`值。

4. **非必须** 创建Telegram 机器人两个参数的 `Secret`：`TELEGRAM_BOT_TOKEN` 和  `TELEGRAM_CHAT_ID`

## 其他服务

- PHP配置: <https://docs.serv00.com/PHP/#php-version>

- Memcached配置: <https://docs.serv00.com/Memcached/>

  启动：memcached -s /usr/home/LOGIN/domains/DOMAIN/memcached.sock -d

- Redis配置: <https://docs.serv00.com/Memcached/>

## 特别注意

serv00虽然有10年使用期，但无法清除Apache和其它服务产生的日志，在容量限制情况下，不建议大日志产生的高流量服务和高频次作业任务。

## JSON生成

- <https://lopinx.github.io/mydevil/>