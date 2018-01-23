## Tomcat配置 {#tomcat}

1.  回到IDEA工程页面，点击右上角图示按钮

![C:\Users\admin\Documents\Tencent Files\385213918\Image\C2C\6BP_6T[_(TUMCN{O]$M7(BO.jpg](../assets/cusersadmindocumentstencent_fi.jpeg)

1.  选择添加local本地tomcat
2.  选择tomcat文件夹
3.  使用Ali-tomcat来启动各个子工程
4.  根据具体情况填写tomcat的相关配置（端口号不能与其他tomcat冲突）

**重要： 在VM options选项中需填写：-Dpandora.location=D:\AliTomcat\taobao-tomcat-7.0.59\deploy\taobao-hsf.sar**

**D：\XXXX\XXX为 淘宝tomcat中taobao-hsf.sar文件的具体路径，请根据实际情况填写。**

1.  点击Deployment，为这个tomcat添加一个模块应用。

（由于我们的开发是基于EDAS分布式，所以我们会把一个工程分割为许多小工程，在开发中，我们需要模拟多台服务器运行不同的模块。所以需要启动多个tomcat将其设置为不同端口。 在每个tomcat上运行独立的模块）

1.  图中带expoloded结尾的为实时更新，当我在代码上进行改动时，tomcat会自动更新。 不带expoloded的为当前代码打成war包发布。
2.  填上项目名
3.  重复上述步骤，为每个模块添加tomcat运行环境。