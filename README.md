适用于易优CMS的payjs支付插件
======
## 前提
已安装好易优CMS

安装文档：https://www.eyoucms.com/help/azwt/2020/1012/11028.html

## 安装

1. 下载插件压缩包：https://github.com/dedemao/eyoucms-payjs/archive/v1.0.0.zip

2. 解压压缩包，将解压后的文件夹覆盖到网站的根目录。

3. 登录后台，启用并设置插件


## 卸载

登录后台，在菜单中选择`插件应用`，点击`卸载`按钮。


## 使用
### 如何支付
指定订单金额：
http://yourname/pay/index?total_fee=0.01

指定订单号：
http://yourname/pay/index?total_fee=0.01&out_trade_no=123456

指定订单标题：
http://yourname/pay/index?total_fee=0.01&subject=测试

指定支付通道：
http://yourname/pay/index?total_fee=0.01&pay_channel=weixin

指定使用JSAPI支付
http://yourname/pay/index?total_fee=0.01&pay_mode=jsapi

指定使用收银台支付
http://yourname/pay/index?total_fee=0.01&pay_mode=cashier

全都指定：
http://yourname/pay/index?out_trade_no=123456&total_fee=0.01&subject=测试&pay_channel=weixin

### 异步通知
异步通知在/application/plugins/controller/Payjs.php中的notify方法

### 退款
退款请参考application/plugins/model/PayjsOrders.php中的refund方法
