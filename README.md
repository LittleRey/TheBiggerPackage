# TheBiggerPackage
饿了么，美团一键领取最大红包APP

## 版本功能

1.在添加页可以登录QQ和绑定手机号缓存帐号

2.小号列表页可管理小号，小号条目侧拉可复制，编辑，删除Cookie。

3.领取页输入红包地址，点击领取可以一键领取到最大红包之前。

4.重置今日领取次数，因为领取的顺序是按照今日领取次数来排序的，为了避免顺序上的效率问题（建议每天重置一下）

5.新人红包提醒，如果是新人号会在领取结束的时候提醒使用者，可以使用满39-15和无门槛红包。


下载地址：https://fir.im/eleme   （这是android APP）


## 界面如下

![界面展示](https://github.com/guoxiaolongonly/TheBiggerPackage/blob/master/screen/main.png)
![小号列表](https://github.com/guoxiaolongonly/TheBiggerPackage/blob/master/screen/setting.png)
![添加小号](https://github.com/guoxiaolongonly/TheBiggerPackage/blob/master/screen/add.png)


## 需求分析

1.用户用的爽，所以只需要用户提供链接和手机号就可以直接领到大红包。

2.API获取，这个需要跟进。饿了么的领取好像不支持外部浏览器，技术难点需要突破，或者做成web页面。

3.从上面的需求可以扩展出，我们需要一堆小号来点红包。

4.由于饿了么验证，我们的小号都需要真实的手机号，所以需要一个获取号码的途径。

5.号码的途径（1.用户手动录入，2.通过短信接收平台获取 例：http://www.51ym.me/User/apidocs.html#errorlist  ）

6.然后就是本地缓存领取次数，防止单个帐号多次点击后续人数不够领大红包。

7.cookie过期处理，提醒用户录入

### 2018年9月19日 更新

了解了一下框架，目前好像只有饿了么，能做抢红包的操作了。
先封装了网络框架，后续会把页面和功能陆续加进来，希望在APP做完之前饿了么的还能用。

### 2018年10月11日 更新

第一版本做完.

大致完成了功能，目前的操作流程如下，

1.通过cookie获取器，拿到QQ授权饿了么的cookie，打开APP，配置，添加号码，把Cookie和QQ号码一起贴上去，保存。

2.通过手机短信验证码获取sid，与cookie绑定，这样一个小号就弄好了。

3.最后面回到首页，输入红包地址，点红包。点到大红包的前一个，不要再点了，复制地址到微信等平台，用自己的大号点开红包（前提是你要有足够多的小号）。

PS：过程有点繁琐，不过大致就是这样了。

第二版本的功能大致会如下

1.优化帐号绑定功能，所有cookie和短信录入通过APP访问饿了么页面获取，一步录入。//已完成

2.帐号录入分为小号和大号，小号列表用来领取小红包，大号专门用来领取大红包。//进行中

3.优化红包获取功能，输入红包地址/sn码，选择大号，点领取，小红包自动由小号领，大号领取大红包。//进行中

4.优化领取功能，当日领取次数最少的小号优先安排领取。//完成

5.接码平台接入（由于接码平台接入存在验证码验证的问题，
所以建议用户直接通过易码接码平台：http://www.51ym.me/User/apidocs.html#login  ）下载相应的应用做操作。

PS:有任何功能上的建议欢迎在issue中提出。


## 免责声明

本项目仅提供技术交流，请勿用于商业及非法用途，如产生法律纠纷与作者无关

## 致谢

协议分享：https://github.com/mtdhb
