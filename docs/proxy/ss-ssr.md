# SS/SSR

!>简单来说代理与VPN的最大区别就在于代理不会虚拟一块独立的网卡<br>
多数的免费代理与VPN有着严格的[NAT类型](4nat.md)，以限制游戏与下载等相关操作

## Shadowsocks

### 入门

访问[ss站点](https://free-ss.tk/)，右键扫描二维码

<!-- ![](https://ipfs.io/ipfs/QmWS9eJJi7dnMXjG7jxYAz7NDDCLHnrtSfc6viNRjbBjc9?2.png) -->

![](https://raw.githubusercontent.com/loremwalker/fq-book/master/docs/images/2018-04-30_105508.png)

 此时已经可以连接互联网了，如果你的系统不是自动设置的，请看<a href="#/proxy/ss-ssr?id=配置">配置</a>

右键允许来自局域网的连接

<!-- ![](https://ipfs.io/ipfs/QmbNUAL9vmXcnAkWP15XxevvLqpED2tbAxxnVCeGDs3o9X?1.png) -->

![](https://raw.githubusercontent.com/loremwalker/fq-book/master/docs/images/2018-05-05_032022.png)

`网络和共享中心`-&gt;`wlan`-&gt;`详细信息`查看本机网卡IP地址

<!-- ![](https://ipfs.io/ipfs/QmdwEi4zS8DNWx8gzkykPAoBkocQguEEP4QYhZFQV8Kwj9?4.png) -->

![](https://raw.githubusercontent.com/loremwalker/fq-book/master/docs/images/2018-05-05_032400.png)

`高级`设置`代理`选择`手动`，按照如下信息设置

<!-- ![](https://ipfs.io/ipfs/QmfU5EVwSUgyNtKFbetxfR1pvcyQTgbmM1y5Rp7QYkuX1b?1.png) -->

![](https://raw.githubusercontent.com/loremwalker/fq-book/master/docs/images/x1.png)

测试

<!-- ![](https://ipfs.io/ipfs/QmRfQ2LhCek5jw7UDBxwC2Y9Qm8VLjP17Ehhgh99Kw7Uod?3.png) -->

![](https://raw.githubusercontent.com/loremwalker/fq-book/master/docs/images/x2.png)

### 配置

有些系统如win7，连接服务器后还需在internet属性中手动设置本机地址与sock5代理端口

<!-- ![](https://ipfs.io/ipfs/QmQBdt4QM9GKcgfFdXh1LtKh45ubyrTqhjEgVHUBk9VfG4?4.png) -->

![](https://raw.githubusercontent.com/loremwalker/fq-book/master/docs/images/2018-04-28_224352.png)

PAC模式即脚本配置模式，收录的网址走代理路线，没有收录的地址则不走代理路线即正常访问。例如将Google加入代理访问列表，配置规则如下：

```text
 ".google.com",
"||google.com",
```

在`pac`选项中-&gt;`编辑本地pac文件`即可

<!-- ![](https://ipfs.io/ipfs/QmeHE8dTsEEQhvQRWBjwzKeioyprepRha6vFFYpce4i22o?1.png) -->

![](https://raw.githubusercontent.com/loremwalker/fq-book/master/docs/images/2018-04-28_230423.png)

## ShadowsocksR

### 订阅功能

如图设置

<!-- ![](https://ipfs.io/ipfs/QmX4z2VDbj5EDvzRzBHTiyqYsTvvxbgDi3pFwhiLfLLNFL?1.png) -->

![](https://raw.githubusercontent.com/loremwalker/fq-book/master/docs/images/2018-04-28_235146.png)

<!-- ![](https://ipfs.io/ipfs/QmNbaKnwt9E447xLzndAZvCHDByMbA6rZn4AsdDbeuFDuP?2.png) -->

![](https://raw.githubusercontent.com/loremwalker/fq-book/master/docs/images/2018-04-28_235317.png)

<!-- ![](https://ipfs.io/ipfs/QmfXCT9yWSxPq4G7QuU9b1RzmFWZodAkY2Pzrt7iGHko5X?1.png) -->

![](https://raw.githubusercontent.com/loremwalker/fq-book/master/docs/images/2018-04-28_235337.png)

<!-- ![](https://ipfs.io/ipfs/QmdteWfXcW3NzJrB8gbxmF83eoybYfBoLThFEC6f8CwYCw?1.png) -->

![](https://raw.githubusercontent.com/loremwalker/fq-book/master/docs/images/2018-04-28_235358.png)

订阅的好处：

* 一键导入多条服务器地址
* 不需要经常打开站点网址即可更新服务器配置（取决于订阅源）

ps:

* ss与ssr的二维码不能通用，否则会出现未扫码二维码的窗口提示
* ss与ssr都做了socks代理端口对http协议的兼容，所以浏览器也是能访问站点的
* 全局模式即被的代理软件所有网络均走代理路线，直连模式即正常访问不走任何代理

