# EBear
**Material Design--Google在I/O 2014上推出了新的设计语言,核心设计原则就是隐喻，视觉设计，动画。引用基友的话就是，遵循用户体验来实现一些让用户用起来舒适满意的动画效果及设计**。CSDN,Github,开源中国上出现了许多优秀的Material Design开源项目，各种好看的库文件也可以直接拿来用，十分方便。

废话不多说，直接上效果图

**1.主界面**
![这里写图片描述](http://img.blog.csdn.net/20160315104131372)


主界面搭建：
Toolbar + DrawerLayout实现的菜单侧滑
PagerSlidingTabStrip+viewpager+fragment实现选项卡左右滑动
RippleEffect实现的点击水波纹效果
RoundImageView实现的圆形头像
FloatActiconButton悬浮按钮的实现
参考资料：

> http://www.jcodecraeer.com/a/anzhuokaifa/androidkaifa/2015/0303/2522.html
> http://blog.csdn.net/lmj623565791/article/details/45303349



**2.滑动变色与下拉缩放**

![这里写图片描述](http://img.blog.csdn.net/20160315104642417)

之前一直想用Toolbar与Palette结合来实现，最后还是采用了监听viewpager的滑动来实现Toolbar的变色
PullToZoomScrollView实现下拉自动放大头部View
参考资料:

> http://blog.csdn.net/bbld_/article/details/41439715
> http://www.jcodecraeer.com/a/opensource/2014/1208/2132.html

**3.头像上传**
![这里写图片描述](http://img.blog.csdn.net/20160315105414474)

Material Dialog:Google Material 风格Android对话框,灵活方便
参考资料:
http://www.open-open.com/lib/view/open1415171087340.html
这里之前一片博客写的很清楚，选择手机相册与拍照上传两种方式

> http://blog.csdn.net/tyk0910/article/details/50236233

**4.修改昵称**
![这里写图片描述](http://img.blog.csdn.net/20160315105600148)

修改完昵称以后，记得在其他界面重写onResume()方法来刷新昵称与头像，达到即时更新效果

**5.修改密码**
![这里写图片描述](http://img.blog.csdn.net/20160315105804800)

TextInputLayout带动画的输入框，这种效果很好的输入框真心值得推荐
参考资料：

> http://www.mamicode.com/info-detail-965904.html

**6.发送文字**
![这里写图片描述](http://img.blog.csdn.net/20160315110017139)

这里有个小细节就是初始化界面的时候，会自动定位到你当前的位置，然后自动显示在地址栏。
CircularProgressButton处理耗时的操作的动画button
参考资料：

> http://blog.csdn.net/hongjinqun/article/details/30221201
> http://blog.csdn.net/tyk0910/article/details/50146149

**7.发送图片**

![这里写图片描述](http://img.blog.csdn.net/20160315110347724)

这个算是APP最难处理的地方了，参考了好多网上的资料进行修改整理，最后达到了这种效果。选择，预览，删除，上传，显示。

**8.点击预览**

![这里写图片描述](http://img.blog.csdn.net/20160315110600005)

CollapsingAvatarToolbar 头像随ListView滚动缩回到ActionBar特效 

原本想预览页面可以用GridView+ImageView实现，后来看到一篇博客，用Dialog实现的，方便又轻巧
参考资料：
http://blog.csdn.net/soul_code/article/details/50448443

**9.下拉刷新与上拉加载**
![这里写图片描述](http://img.blog.csdn.net/20160315110848244)

需要注意的是分页查询的使用与显示
Android SwipeRefreshLayout下拉刷新与上拉加载，之前一片博客说的很清楚：

> http://blog.csdn.net/tyk0910/article/details/50427531

**10.登录注册**
![这里写图片描述](http://img.blog.csdn.net/20160315111102102)

切换账号的时候，记得清空缓存再进行登录注册。

**11.服务器后台**

我用的是Bmob后端云，所有数据都是从上面存储与读取的，开发文档很详细。这是部分数据截图
![这里写图片描述](http://img.blog.csdn.net/20160315111436314)
参考资料:

> http://www.bmob.cn/


**12.其他技术**
图片的上传，下载，缓存，我用的是Universal-Image-Loader来异步加载网络图片：
参考资料：
http://blog.csdn.net/tyk0910/article/details/50375070

回调的使用：
http://blog.csdn.net/tyk0910/article/details/50564917

其他就是数据的显示，更新，存储，读取，按照开发文档以及业务逻辑就行

最后就是贴一下使用的库文件以及jar包：
![这里写图片描述](http://img.blog.csdn.net/20160315112021025)

![这里写图片描述](http://img.blog.csdn.net/20160315112035182)


项目还存在不少小问题，就在Pre.im上发布了一下。
![这里写图片描述](http://img.blog.csdn.net/20160315112435124)
地址：

> http://pre.im/ebear

最近忙着准备面试，目前就先做到这里。以后陆陆续续肯定会加入其它的功能，点赞评论加关注什么的。

代码也同步到了github上欢迎大家一起交流。欧了，源码地址：
https://github.com/18722527635/EBear
