# java日常

>有一些不知道这么分类就放里面吧
>
## 2021

+ 2021/7/27 [java-fix序列化漏洞](java-fix序列化漏洞.md)
+ 2021/7/28 [java执行js导致命令执行](java执行js导致命令执行.pdf)
+ 2021/7/28 [java反射](./img/反射.png)
+ 2021/7/29 [反射newInstance的使用方式](反射newInstance的使用方式.md)
+ 2021/8/18 [java-maven打包学习](java-maven打包学习.md)
+ 2021/8/18 [java基础-编译运行原理](https://fantiq.github.io/2019/08/13/java%E5%9F%BA%E7%A1%80-%E7%BC%96%E8%AF%91%E8%BF%90%E8%A1%8C%E5%8E%9F%E7%90%86/)
+ 2021/8/19 [java-xxe学习1](https://github.com/gyyyy/footprint/blob/master/articles/2018/xxe-injection-overview.md)
+ 2021/8/19 [探究Java中XXE漏洞的深层原理](https://gv7.me/articles/2019/study-the-deep-principle-of-xxe-vulnerability-in-java/)
+ 2021/8/19 [xxe流程图](./img/xxe.png)
+ 2021/8/20 [jep290的实现图片](./img/jep290.png)   [文章](https://y4er.com/post/bypass-jep290/)
+ 2021/8/31 [java写文件rce](java写文件rce.md)
+ 2021/8/31 [java协议](java协议.md)
+ 2021/9/01 [java反序列化编码绕过](java反序列化编码绕过.md)
+ 2021/9/03 [javabean与内省](javabean与内省.md)
+ 2021/9/03 [marshalsec工具使用](marshalsec.md)
+ 2021/9/03 [readobject深入](readobject深入.md)
+ 2021/9/03 [Thinking in java 高级之volatile](Thinking_in_java高级之volatile.md)   volatile如果对应单线程会不会存在条件竞争问题 参考d3ctf no rce
+ 2021/9/03 [yso搭建](yso搭建.md)
+ 2021/9/14 [yso中gadget的问题，有一个gadget正在泄露你的ID](https://mp.weixin.qq.com/s?__biz=Mzg3NjA4MTQ1NQ==&mid=2247484138&idx=1&sn=55d82300e8ffd567610926d887b42afc&chksm=cf36faaaf84173bc733c94198df766fd02f0309dd48882aba5847e0dcc8d6b57a0141183c4f3&mpshare=1&scene=23&srcid=0914UihVLrgENHy1xcbuIGIX&sharer_sharetime=1631594366441&sharer_shareid=33a823b10ae99f33a60db621d83241cb#rd)         个人感觉思路非常非常好。思路开拓。
+ 2021/9/14 [Java动态类加载，当FastJson遇到内网](https://kingx.me/Exploit-FastJson-Without-Reverse-Connect.html)   **个人感觉其中的fastjson触发特定的getter说的比较清楚，如果是parseObject，就会将Java对象转为JSONObject对象即调用JSON.toJSON，在处理过程中会调用所有的 setter 和 getter 方法。而如果是parse方法，原理是fastjson反序列化是生成了一个jsonobject,而JSONObject放在JSON Key的位置上，在 JSON 反序列化的时候，FastJson又会对JSON Key 自动调用 toString() 方法**
+ 2021/9/15 [FastJson反序列化漏洞利用的三个细节 - TemplatesImpl的利用链](https://kingx.me/Details-in-FastJson-RCE.html)
+ 2021/9/18 [Java 反序列化漏洞始末（3）— fastjson](https://b1ue.cn/archives/184.html)
+ 2021/9/18 [log4j<=1.2.17反序列化漏洞（CVE-2019-17571）分析](https://mp.weixin.qq.com/s?__biz=Mzg3NjA4MTQ1NQ==&mid=2247483962&idx=1&sn=0e059564c368b84e3483704821aac06b&chksm=cf36fa7af841736c622b957459091f3dd994adbfbc8bf8bcab032995c0885776c62530eaf465&mpshare=1&scene=23&srcid=0918r2rgVPTbTKFRbVikY7cS&sharer_sharetime=1631972571155&sharer_shareid=33a823b10ae99f33a60db621d83241cb#rd)  **log4j组件存在反序列化漏洞端口4560**
+ 2021/9/24 [搞懂RMI、JRMP、JNDI-终结篇](https://threedr3am.github.io/2020/03/03/%E6%90%9E%E6%87%82RMI%E3%80%81JRMP%E3%80%81JNDI-%E7%BB%88%E7%BB%93%E7%AF%87/)  **LDAP服务攻击一般是先测Reference再测deserializeObject**
+ 2021/9/25 [JAVA Apache-CommonsCollections 序列化漏洞分析以及漏洞高级利用](https://www.iswin.org/2015/11/13/Apache-CommonsCollections-Deserialized-Vulnerability/)  [实现代码](https://github.com/Firebasky/Java/tree/main/java%E5%9B%9E%E6%98%BE)
+ 2021/9/26 [gradle和maven有什么用？分别有什么区别](https://www.zhihu.com/question/29338218)  **简单的了解了一下gradle项目搭建**
+ 2021/9/27 [java 反序列化 ysoserial exploit/JRMPClient 原理剖析](https://dandelioncloud.cn/article/details/1432371613173100545/) **简单的说让靶机反序列化payloads/JRMPListener进行开启rmi端口，然后使用exploit/JRMPClient去连接并且发送payload反序列化攻击，是利用DGC通信的。JEP 290之后就不行了。**
+ 2021/9/27 [java 反序列化 ysoserial exploit/JRMPListener 原理剖析](https://dandelioncloud.cn/article/details/1432371613252792321) **简单的说自己的vps上开启jrmp服务监听，靶机反序列化payloads/JRMPClient 然后来连接我们的vps，我们在发送payload进行反序列化，原理也是利用DGC通信的。在使用this.classLoader.loadClass加载时，可以来绕过。** 见：
+ 2021/10/2 [缩小ysoserial payload体积的几个方法](https://xz.aliyun.com/t/6227) **原理上是通过createTemplatesImpl去实现的** 说不定有时候会遇到呢？
+ 2021/10/3 [Java 实现后台执行](https://jayl1n.github.io/2020/02/13/java-nohup-implementation/)
+ 2021/10/3 [Java项目中常见jar包的说明](https://www.mi1k7ea.com/2019/11/25/%EF%BC%88%E8%BD%AC%EF%BC%89Java%E9%A1%B9%E7%9B%AE%E4%B8%AD%E5%B8%B8%E8%A7%81jar%E5%8C%85%E7%9A%84%E8%AF%B4%E6%98%8E/)  **熟悉一些jar包了解了解**
+ 2021/10/3 [XXL-JOB Hessian2反序列化漏洞](https://www.mi1k7ea.com/2021/04/22/XXL-JOB-Hessian2%E5%8F%8D%E5%BA%8F%E5%88%97%E5%8C%96%E6%BC%8F%E6%B4%9E/)
+ 2021/10/3 [Java代码反反编译对抗思路](https://www.mi1k7ea.com/2020/05/01/Java%E4%BB%A3%E7%A0%81%E5%8F%8D%E5%8F%8D%E7%BC%96%E8%AF%91%E6%80%9D%E8%B7%AF/) **之前自己想通过加密class实现，不过不是特别通用就没有写了。。。。**
+ 2021/10/10 [XXE漏洞利用技巧：从XML到远程代码执行](https://blog.csdn.net/u012206617/article/details/109038388) **其中总结的xxe利用非常好，还有挖掘思路和netdoc协议和jar协议，还有自定义http访问延迟连接保证临时文件不被快速删除**
+ 2021/10/19 [JAVA代码审计业务安全Checklist](https://mp.weixin.qq.com/s?__biz=MzI5MDU1NDk2MA==&mid=2247500712&idx=1&sn=13027edf1e9d3385b650e611e9f559ab&chksm=ec1c9697db6b1f812fd88463a8d8301303b8c7cc364497d2ce1ca2190cf96701ad25463fc01d&mpshare=1&scene=23&srcid=1018GCa0aDvbQenw0fTuSv6F&sharer_sharetime=1634527194186&sharer_shareid=33a823b10ae99f33a60db621d83241cb#rd)  **代码审计比较帮助**
+ 2021/10/19 [在Jfinal使用redis缓存时存在的反序列化问题](https://b1eed.github.io/2020/12/05/Jfinal_readObject/) **这个和CVE-2020-26945 mybatis二级缓存反序列化有异曲同工之妙**
+ 2021/10/21 [自定义ClassLoader绕过poc为什么很多人执行出现问题的缘由](https://github.com/codeplutos/java-security-manager-bypass/issues/2) **可能以后会遇到。**
+ 2021/10/25 [defineClass在java反序列化当中的利用](https://paper.seebug.org/572/)  defineClass可以从byte[]还原出一个Class对象 **org.mozilla.classfile.DefiningClassLoader#defineClass**
+ 2021/10/26 [浅析JDWP远程命令执行漏洞](https://www.mi1k7ea.com/2021/08/06/%E6%B5%85%E6%9E%90JDWP%E8%BF%9C%E7%A8%8B%E4%BB%A3%E7%A0%81%E6%89%A7%E8%A1%8C%E6%BC%8F%E6%B4%9E/) 大概就是开启了远程Debugger..
+ 2021/10/26 [浅析Ofbiz反序列化漏洞CVE-2020-9496](https://www.mi1k7ea.com/2021/09/21/%E6%B5%85%E6%9E%90Ofbiz%E5%8F%8D%E5%BA%8F%E5%88%97%E5%8C%96%E6%BC%8F%E6%B4%9E%EF%BC%88CVE-2020-9496%EF%BC%89/) 版本小于17.12.04 
+ 2021/10/26 [Hessian 原理分析](https://www.cnblogs.com/shangxiaofei/p/4222170.html) 大概就是以二进制数组传输的rpc，存在反序列化问题。
+ 2021/10/26 [XXL-JOB Hessian2反序列化漏洞](https://www.mi1k7ea.com/2021/04/22/XXL-JOB-Hessian2%E5%8F%8D%E5%BA%8F%E5%88%97%E5%8C%96%E6%BC%8F%E6%B4%9E/)
+ 2021/10/30 [Mojarra JSF ViewState 反序列化漏洞](https://blog.csdn.net/xuandao_ahfengren/article/details/113135364) 
+ 2021/11/02 [关于Java 中 XXE 的利用限制探究](https://www.freebuf.com/articles/web/284225.html) **使用http外带数据不能有换行，使用ftp可以解决，但是ftp在java 8u131修复了这个漏洞 CVE-2017-3533**
+ 2021/11/02 [Adobe ColdFusion 反序列化漏洞（CVE-2017-3066）](https://github.com/vulhub/vulhub/blob/master/coldfusion/CVE-2017-3066/README.zh-cn.md) 暴露接口反序列化。。。
+ 2021/11/03 [浅谈Liferay Portal JSON Web Service未授权反序列化远程代码执行漏洞](https://xz.aliyun.com/t/7485)
+ 2021/11/03 [H2 Database Console 未授权访问](https://github.com/vulhub/vulhub/blob/master/h2database/h2-console-unacc/README.zh-cn.md)
+ 2021/11/30 [wsdl相关](wsdl.md) **接触到一些soap协议。。。**
+ 2021/12/11 [log4j 漏洞一些特殊的利用方式](https://mp.weixin.qq.com/s?__biz=Mzg4OTExMjE2Mw==&mid=2247483945&idx=1&sn=b15b68d95da83bb20f1b3496396f823a&chksm=cff19125f88618338373a32f98be3d2a9497b464d6531658c2aa96f4872c23eed294441917b5&mpshare=1&scene=23&srcid=1211aS0Tghr1agBnBRlwwGTw&sharer_sharetime=1639232420884&sharer_shareid=33a823b10ae99f33a60db621d83241cb#rd) **自己也发现了这个利用思路，不过不知道ResourceBundle类是干什么的。。。。** https://www.cnblogs.com/jona-test/p/11399218.html  **用来读取项目中后缀为properties的配置文件，然后通过dnslog或者ldap回显示**
+ 2021/12/13 [Java读文件](https://www.cnblogs.com/hkgov/p/14707726.html) **方便操作。。。**
+ 2021/12/14 [不使用new创建对象](https://zhuanlan.zhihu.com/p/214093086) **unsafe.allocateInstance()** [unsafe使用](https://tech.meituan.com/2019/02/14/talk-about-java-magic-class-unsafe.html)
+ 2021/12/14 [Spring Boot中关于%2e的Trick](http://rui0.cn/archives/1643)
+ 2021/12/18 [闲谈log4j2](闲谈log4j2.md)
+ 2021/12/19 [SPI机制](SPI机制.md)
+ 2021/12/21 [从一个被Tomcat拒绝的漏洞到特殊内存马](https://xz.aliyun.com/t/10577) **简单的说就是Tomcat启动时会加载lib下的依赖jar，如果黑客通过上传漏洞或者反序列化漏洞在这个目录添加一个jar，重启后，某些情况下这个jar会被当成正常库来加载，在一定条件下造成RCE** 这个功能是非常正常的因为中间件的类加载机制不是双亲委派机制.都是自己实现的
+ 2021/12/23 [寻找复杂对象的属性值](searchobj.md) **是在使用object-searcher的时候想到了，于是去学习了一下在java中通过递归去寻找复杂对象的属性。**
+ 2021/12/29 [jps命令](https://www.cnblogs.com/keystone/p/10789382.html) **其中可以支持远程调用并且默认情况下， jstatd开启在1099 端口上开启RMI服务器，rmi服务？想到了什么！**
+ 2021/12/30 [浅谈Log4j2不借助dnslog的检测](https://xz.aliyun.com/t/10676) **还得是大哥，思路太棒了，通过tcp数据传输的方面来验证漏洞。。学习！**
+ 2021/12/31 [构造java探测class反序列化gadget的思考](构造java探测class反序列化gadget的思考.md) **2021 新年快乐**

## 2022
+ 2022/01/07 [GadgetProbe：利用反序列化来暴力破解远程类路径](https://bishopfox.com/blog/gadgetprobe) **和构造java探测class反序列化gadget的思考思路是一样的**
+ 2022/01/08 [目录穿越上传](https://github.com/metersphere/metersphere/issues/8653) **tw上有一个后台上传jar插件进行getshell的**
+ 2022/01/08 [关于 Java 中的 RMI-IIOP](https://paper.seebug.org/1105/) **没有这么看懂。23333**
+ 2022/01/08 [你了解 SpringBoot java -jar 的启动原理吗？](https://xie.infoq.cn/article/765f324659d44a5e1eae1ee0c) 
+ 2022/01/08 [c语言能不能实现agent?](c语言能实现agent%3F!.md) **通过编写c语言代码去实现agent**  **实现了通用的代码https://gist.github.com/Firebasky/c1efd9dc7eb964a77cb788c170a8598f**
+ 2022/01/09 [瞒天过海计之Tomcat隐藏内存马](https://tttang.com/archive/1368/) 思路是[从一个被Tomcat拒绝的漏洞到特殊内存马](https://xz.aliyun.com/t/10577)中不过使用了agent去实现并且工具化了，太猛了(有空学习一下ysomap。。。。
+ 2022/01/09 [入侵JVM?Java Agent原理浅析和实践中](https://blog.csdn.net/CringKong/article/details/120840827)
+ 2022/01/09 [Java内存攻击技术漫谈](https://xz.aliyun.com/t/10075) **神仙级别的文章，还没有看完23333，慢慢消化** 
+ 2022/01/09 [解决agent中tools加载的问题](解决agent中tools加载的问题.md) **学习思路**
+ 2022/01/10 [unsafe学习](unsafe学习.md) **可以用来bypass 反射filter**
