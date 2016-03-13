# Swift和C混合Socket编程实现简单的ping命令
# 使用Swift进行主机发现和MAC地址解析

![](/xwjack.gif?raw=true)

![](/xwjack1.png?raw=true)

![](/xwjack2.png?raw=true)

更新于2016-3-13
新增主机发现功能,mac地址解析功能,本机mac不能使用,用xx:xx:xx:xx:xx:xx代替.获得WiFi的ssid和bssid.
程序依旧有许多不足的地方,如果有大神,希望帮我改改.
不足:
1.没有运行循环,用的是超时.
2.有时候会出现连续发送icmp失败的情况.
3.再次刷新的时候会出现bogon变成unknow的情况.
4.主机发现是根据stackoverflow上面的代码改编的.应该是读取arp缓存表,但是前提是发送icmp来刷新缓存表.
发送icmp数据包是多线程异步并列的形式发送.线程这里没有处理好,当学会了之后再更新.
5.那个进度条还没有添加,给人感觉是卡死的.
以上的问题会进一步更新.

由于只能在真机上调试,所以只能是截图,不能看到动态图.
如果想看详细的代码解释说明,请到我的博客.


更新于2016-1-13
修复bug,优化部分显示,更好,更安全的处理指针类型.

更新于2016-1-12
新增功能:优化显示,将返回的结果显示到模拟器中.发送数据包在额外的线程中进行,不会阻塞主线程.由于程序使用的是Swift和C语言混合编程,用到了指针,交互的时候容易crash.后续会继续修复bug.

更新2016-1-7
新增功能:优化显示,将返回结果集中到主函数中,方便调用,修复部分bug,添加超时处理,防止程序一直处于阻塞状态

# MyBlog
http://www.cnblogs.com/xwjack1554239786/p/5131787.html
