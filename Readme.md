###摘要: 用H5实现调用系统电话

##1、需求描述

    在ionic项目用调用手机的打电话功能。开始还想找cordova和ng-cordova的插件那，现在H5实现起来特别方便。

##2、准备

    在cordova中所有的URL Schemes 都是服从于白名单的，所以要现在项目config.xml中添加

<access origin="tel:*" launch-external="yes" />

    Making a Phone Call from Within PhoneGap in Android and iOS

##3、代码实现

    ###①html代码直接写就可以了

        <a href="tel:15210203452">打电话</a>
        <a href="tel:10086">打10066</a>

    ###②在controller中实现也就一句话

$scope.callPhone=function(){

    $window.location.href="tel:10085";

}
##4、扩展阅读

### ① iOS的实现需要借助插件，具体参照链接资料。 

    http://rickluna.com/wp/2012/02/making-a-phone-call-from-within-phonegap-in-android-and-ios/

### ②手持移动端特殊链接：打电话，发短信，发邮件



##5、URL Schemes

这个东西貌似直接用的话只能在ios中用

如何找到软件的URL Schemes？

http://www.zhihu.com/question/19907735

自定义URL scheme for iOS与Android

但是在AIR apps中用自定义URL schemes调用别的apps是不允许的，AIR的安全模型对于schemes在http:，sms：，tel: ，mailto:， file:  ，app:  ，app-storage: ，vipaccess:和connectpro:中的限制是很严格的。



## ios

http://jbguide.me/2015/03/21/launcher/



## android

http://www.360doc.com/content/14/0901/16/9200790_406290994.shtml

http://www.w3chtml.com/html/url.html

