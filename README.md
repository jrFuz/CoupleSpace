# CoupleSpace
我的第一个完整的JavaWeb项目——情侣日志网站。现已部署上线，请移步 www.ygj0930.com 体验。
这个情侣日志网站的灵感主要是“一张照片一个故事”这个主题，网站提供了情侣们分享ta们的情感事件的功能，每篇日志可以搭配图片进行叙事。

CoupleSpace1.0:
项目使用了三层架构——视图层、控制层、业务层，使用了vo、dto封装类实现各层架构之间数据传递。
登录与注册时的验证码使用了自己写的算术验证码图片生成类。
日志部分用了Ueditor插件实现内容输入，图片上传用了自己写的文件上传处理类。
日志列表部分用了数据库分页查询来实现列表的分页显示.
分页查询部分用了一个中间表来记录日志总数，优化了分页查询，原理见我的博文http://www.cnblogs.com/ygj0930/p/6138288.html

CoupleSpace2.0:
增加了监听器和过滤器：
用监听器实现了在线人数统计，监听session的建立和销毁来统计在线人数。原理见我的博文：http://www.cnblogs.com/ygj0930/p/6374384.html
用过滤器实现统一编码格式设置以及登录权限限制，通过检测session中的userid属性判断用户是否登录，没有登录的用户不能访问日志列表等资源，自动跳转到登录页面。原理见我的博文：http://www.cnblogs.com/ygj0930/p/6374212.html
