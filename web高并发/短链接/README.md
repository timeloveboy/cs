# 短链接 生成原理


+ 发号策略

正确的原理就是通过发号策略，给每一个过来的长地址，发一个号即可，小型系统直接用mysql的自增索引就搞定了。如果是大型应用，可以考虑各种分布式key-value系统做发号器。不停的自增就行了。第一个使用这个服务的人得到的短地址是http://xx.xx/0 第二个是 http://xx.xx/1 第11个是 http://xx.xx/a 第依次往后，相当于实现了一个62进制的自增字段即可

作者：iammutex
链接：https://www.zhihu.com/question/29270034/answer/46446911
来源：知乎
著作权归作者所有。商业转载请联系作者获得授权，非商业转载请注明出处。