Java版本，教程最近一次更新时间为：2022-10-27
# CSDN是旧版，请参考下面的最新教程。包含小白教程

## CSDN不能放联系方式，我就放置顶这里了



QQ群：

![image-20220914164151679](https://i0.hdslb.com/bfs/album/7680c403a1c05bb16e277e90e9f7a0985c3f3c58.png)

作者联系方式：

..

打扰太多，转为qq群上解决问题，有什么问题直接问即可。

# 目录：

[1.通用准备](#通用准备)

[2.面向开发者](#面向开发者)

[3.面向小白](#面向小白)

[4.联系作者](#联系作者)

[5.常见问题](#常见问题)

# 通用准备

## 1.1 申请微信公众号

[点击跳转申请](https://mp.weixin.qq.com/debug/cgi-bin/sandbox?t=sandbox/login)

- 得到这个页面：

![image-20220825095034745](https://i0.hdslb.com/bfs/album/283615dd5ef3d5d83936b61f08bf1bd8277a3393.png)

- 滑到下面，**扫码**关注公众号

  ![image-20220825095130874](https://i0.hdslb.com/bfs/album/8c11064fda79d3a563bb4358c04a3e0627d0e9ac.png)

- 新增模板,【中文】的可以改，{{xxx.DATA}}不能改，但可以移动位置。

  ```te
  {{first.DATA}}
  
  城市：{{city.DATA}}
  
  实况天气：{{weather.DATA}}
  气温：{{minTemperature.DATA}} ~ {{maxTemperature.DATA}}
  风速：{{wind.DATA}}
  湿度：{{wet.DATA}}
  今天~后天：{{day1_wea.DATA}},{{day2_wea.DATA}},{{day3_wea.DATA}}
  
  ♥在一起♥: {{togetherDate.DATA}}
  
  距离kk生日：{{birthDate1.DATA}}
  距离gg生日：{{birthDate2.DATA}}
  
  {{note_En.DATA}}
  
  {{note_Zh.DATA}}
  ```

  ![image-20220825112223388](https://i0.hdslb.com/bfs/album/5645048e9396ff8c2b981e05bf12a06ae60bad0e.png)

  ![image-20220825112250898](https://i0.hdslb.com/bfs/album/541e1dfdf5577cba964f9d78c1ce28ed62fc3c45.png)

## 1.2 申请天气接口

[点击注册并申请](https://tianqiapi.com/user/login)

- 完成注册登录后得到下面这个页面

  ![image-20220825095436327](https://i0.hdslb.com/bfs/album/fb74d65dc2e2a116e54dc1ba6e61a054aa40d747.png)

## 1.3 名言名句申请

[点击注册](https://www.apispace.com/eolink/api/myjj/introduction)，可有可无，不申请推送效果如下（左边申请的，右边不申请）。

![image-20220901201425210](https://i0.hdslb.com/bfs/album/10bf14bb5c141a68cbdb24f740fbb551a54699e8.png)



![image-20220825095959904](https://i0.hdslb.com/bfs/album/311a3f14f84876567603cbfc92cea3f01d6fd720.png)

- 购买接口，用新人券，券自动送的，【直接白嫖1k次】~

  ![image-20220825110802433](https://i0.hdslb.com/bfs/album/ec38f3d30176d476db64b6835a068438b4d91438.png)

- 找到Token

  ![image-20220825110959444](https://i0.hdslb.com/bfs/album/dd9e16fb65e34e91a3f4b17f96962f5446db517f.png)

# 面向开发者

## 2.1 克隆项目

- 打开Idea

  ps：idea是一款适合Java开发的一款编辑器软件，如有需要可以自行百度安装并完成破解。

  ​	参考链接：[IntelliJ IDEA 2022.2.3最新激活破解教程（永久激活，亲测有效） - 异常教程 (exception.site)](https://www.exception.site/essay/how-to-free-use-intellij-idea-2019-3)

  ![image-20220825111147034](https://i0.hdslb.com/bfs/album/e35c4a638aa22fa49fcfcf761cda3d539e9c93e4.png)

- 克隆我的GitHub项目。

  找到idea的左上角new一个项目。

  ![image-20221027004950055](https://i0.hdslb.com/bfs/album/18dd7307e659006d96026ee61e6dfd4e57f02f5a.png)
  
  地址：https://github.com/qq1534774766/wx-push.git
  
  Directory你随意，只是项目存放地址。
  
  ![image-20220825111225911](https://i0.hdslb.com/bfs/album/139e2c9a7370c2c9d5c1517f17ae9a67302b09b3.png)

## 2.2 配置文件

![image-20220825111704640](https://i0.hdslb.com/bfs/album/40ae4dbfa1a0d52b95c75eaf7ab8814f15fbb107.png)

- 看以下图片配置即可

  - ApiSpace: token: 是名言名句，没有申请的话，略过即可。
  - **注意：**city，不可能添加省市区字符，如广东省广州市海珠区，只能写成**海珠**
  
  ![ad8627f27c8601f06c828d43a233e8af74af444d](https://i0.hdslb.com/bfs/album/18c0a3ad2ada6ff81f8ab016b5797ab2191319f9.png)



## 2.3 使用

1. 找到WxPushApplication，运行main方法即可。

   ![image-20221027005250382](https://i0.hdslb.com/bfs/album/1cb869ef747e2c5368e5ac83ae60c64f524dafec.png)

   如提示图示，表示运行成功：

   ![image-20221027005422431](https://i0.hdslb.com/bfs/album/006b926e0706706f24ff0cfe7df9d097a36bf5a7.png)

2. 打开浏览器访问：http://localhost:8081/send  即可收到公众号的推送信息

   ![image-20220902103432701](https://i0.hdslb.com/bfs/album/f57b1e358a5c328fb3bca4c0b12234d9044eec84.png)

3. 修改城市：打开：http://localhost:8081/  即可打开网页，输入新城市点击提交即可。

   ![image-20220902103445431](https://i0.hdslb.com/bfs/album/0311ee56377bcf330a2fc024c7d8dff5c4601811.png)

## 2.4 高级

### 2.4.1 本地自动推送

- 那就是让自己运行项目的电脑不关机即可~

- 默认是每天早上7:30推送，可以自己修改

![image-20220825113234321](https://i0.hdslb.com/bfs/album/0913a49e509856ed4c6364a85cd9d75ff74014fc.png)

### 2.4.2 云服务器自动推送

- 如果你有云服务器，就能实现24h自动推送啦

- 简单讲解，

  - 打包

    ![image-20220825114120159](https://i0.hdslb.com/bfs/album/e934c8693c0a5b6b252f33e682fe1c04ee92c6a0.png)

  - 部署

    ![image-20220825114149760](https://i0.hdslb.com/bfs/album/cfa98f1a7d73d6958adc45abae9cfd2c304e74c8.png)

    ------------------------------------------------------

    ![image-20220825114220959](https://i0.hdslb.com/bfs/album/d319b4c48a2319abf24e12e51a08fca0cb2f7f27.png)

  - 上传

    这里我使用的是MobaXterm终端管理软件。

    下载链接：https://download.mobatek.net/2212022060563542/MobaXterm_Installer_v22.1.zip

    下载完解压后安装即可。（安装可能会遇到提示3503等错误无法安装，那是因为安装程序的权限不够，选中安装包选择以管理员身份运行即可。）
  
    上次步骤如图：

    1. ![image-20221027010632537](https://i0.hdslb.com/bfs/album/53b749e9641594d7dc87c86f502d187c2af6b2f5.png)
    2. ![image-20221027010719886](https://i0.hdslb.com/bfs/album/903e2201d01aabc4c64c4be659b73b09ef803bad.png)
    3. ![image-20220825114527103](https://i0.hdslb.com/bfs/album/dfca31d85e2c663be077f2dedb706c62668d4555.png)

    然后运行指令：

    ```bash
    nohup java -jar wx.jar >wx.txt &
    ```
  
    这里输入命令一路回车即可，没有什么特别的提示。
  
    ![动画2](https://i0.hdslb.com/bfs/album/c9385c90faecda4e204cf5fee5f6bbb7ba0094bc.gif)
  
  - 放行端口
  
    因为默认是8081的端口，**务必**要开放服务器的防火墙！！！！
  
    下面是阿里云的示例
  
    - ![image-20220901205911423](https://i0.hdslb.com/bfs/album/0c64b00474c62baadd4d3bb7c615a11e62768975.png)
  
    
  
    
  
    - ![image-20220901205842009](https://i0.hdslb.com/bfs/album/95fa6d131081759f8950c16e46476857751350db.png)
  
    
  
  测试：1.0.0.0是你的服务器ip地址
  
  **作废：**因为公共路径wx并没用配置，所以会导致404
  
  ~~http://1.0.0.0:8081/wx/send   推送~~
  
  ~~http://1.0.0.0:8081/wx  修改天气城市~~
  
  **正常：**
  
  http://公网IP:8081/send   推送
  
  http://公网IP:8081/  修改天气城市

## 2.5 2022年9月01日问题修复

- 如果会用git的话，可以直接拉取最新代码即可。

![image-20220901200626974](https://i0.hdslb.com/bfs/album/8cbfc2b9680b460fec02b99d4531fcd0f886ec74.png)

- 如果不会用git，则建议重新克隆项目[2.1 克隆项目](##2.1 克隆项目)，application.yaml文件记得备份一份到桌面，以免被覆盖掉。

**注意**：新的application.yaml，新增了一个属性

![image-20220901202405807](https://i0.hdslb.com/bfs/album/173a658fce449d2f16aac6315b5f8cfe19832ab6.png)

如果你想要名言名句，务必设置为**TRUE**

以下是问题修复日志，给喜欢探究问题原因的伙伴食用。

### 2.5.1 天气修复

1. 从天气api获取到，未来的天气的日期是 01  02  03 的两位数的形式。
2. Java中的LocalDate类提供的日期，是一位数的 1  2  3 的形式
3. 因为一开始用是String字符串类型比较，所以01≠1，最后导致天气无法获取。

### 2.5.2 名言警句修复

- 获取的句子不正常
  - 因为博主为了测试功能，使用的是免费的接口。
  - 使用免费公开的api https://api.xygeng.cn/one ，其句子收集自各个平台，所以会出现**贬义**的意思。

所以，现在已经修改为收费的apispace。这个你已经申请过了，就是[上面【1.3 名言名句申请】](##1.3 名言名句申请)

### 2.5.3 名言警句可以手动开启

- application.yaml文件中

  ![image-20220901202235041](https://i0.hdslb.com/bfs/album/dfc5969d77eb0ad7f629775c0f0cbad992d79986.png)

  enableDaily属性，可以配置是否开启每日一句。

  **注意**：公众号的模板**无需**做出任何改变

# 面向小白

两种小白：1.外行小白。2.非Java出身的IT小白

外行小白这部分只看：3.1~3.4就好。

非Java出身的IT小白：全可看

## 3.1 安装Java环境

Java环境就是运行这个应用的基本要求，电脑必须要安装和配置才能正确的运行Java程序。

- 安装Java的教程网上特别多，这里推荐一篇博客，Java安装包我已提供，[点击打开CSDN安装Java教程](https://blog.csdn.net/wumingxiaozei/article/details/95628747)

- Java安装包、wx.jar下载，提供阿里云：

  > 「微信推送-小白版」，点击链接保存，或者复制本段内容，打开「阿里云盘」APP ，无需下载极速在线查看，视频原画倍速播放。 链接：https://www.aliyundrive.com/s/JFcZ2F7Lj5c

![image-20220902110558803](https://i0.hdslb.com/bfs/album/89a48314970651f7d61d875cf6c6f3aa62e57d98.png)



## 3.2 配置wx.jar

1. 右键选择文件，使用解压软件打开，不用解压

2. 找到配置文件，wx.jar/BOOT-INF/classes，下的application.yml文件

   ![image-20220902093420949](https://i0.hdslb.com/bfs/album/93da3bacb49f216a2cda01f0548dad9643d304a3.png)

3. 双击，使用文本编辑器 (记事本)打开

   ![image-20220902093543737](https://i0.hdslb.com/bfs/album/fbdf33f986bfcf1327bcece186e4aa7ba818c13e.png)

4. 看以下图片配置即可

   - ApiSpace: token: 是名言名句，没有申请的话，略过即可。

   ![ad8627f27c8601f06c828d43a233e8af74af444d](https://i0.hdslb.com/bfs/album/18c0a3ad2ada6ff81f8ab016b5797ab2191319f9.png)

5. 保存文件，并更新。

   选择确定

   ![image-20220902093859624](https://i0.hdslb.com/bfs/album/a30c00f0267eed92e3d19343b3a6b275a30b441a.png)

6. 配置自动推送的时间

   默认是7.30，没有代码编辑器无法修改，可以联系作者修改，有空就改



## 3.3 运行wx.jar

![动画1](https://i0.hdslb.com/bfs/album/de2b199ed21eebceb6672a4b15a10a6bf0c1321d.gif)

这样就成功启动了~

## 3.4 使用

1. 打开浏览器访问：http://localhost:8081/send  即可收到公众号的推送信息

   ![image-20220902103432701](https://i0.hdslb.com/bfs/album/f57b1e358a5c328fb3bca4c0b12234d9044eec84.png)
3. 修改城市：打开：http://localhost:8081/  即可打开网页，输入新城市点击提交即可。

   ![image-20220902103445431](https://i0.hdslb.com/bfs/album/0311ee56377bcf330a2fc024c7d8dff5c4601811.png)

## 3.5 服务器自动推送

- 上传到Linux云服务器

![image-20220825114527103](https://i0.hdslb.com/bfs/album/dfca31d85e2c663be077f2dedb706c62668d4555.png)

- 启动

  ![动画2](https://i0.hdslb.com/bfs/album/c9385c90faecda4e204cf5fee5f6bbb7ba0094bc.gif)

# 更多

## 4.1 关于模板定制

模板可以直接改布局的，中文随意改变，但是 {{xxx}}内容不能改，可以移动位置。

你可以在模板随意追加想要的句子，但要注意公众号的推送是有篇幅限制的，不宜太长。

注意：更新模板后，同时需要在application.yml文件更新模板ID.

![image-20220902164806318](https://i0.hdslb.com/bfs/album/235d8b6e4957aa0e3d2f17e031ff5a04cffd9a32.png)

## 4.2 关于自动推送

- 自己的电脑不关机，充当服务器，默认每天早上7.30自动推送，可以修改时间的，看 2.4.1本地自动推送。
- 云服务，这个需要购买服务器才行，建议有Linux基础的人动起手来。

# 联系作者

wx:Potato_Sgr

qq:1534774766

# 常见问题

提问问题前，看看这里。

1. 项目无法启动，启动报错
   - 检查电脑java环境安装是否成功？win+r 输入cmd 回车，输入命令 java -version ，有显示版本信息才表示正常。
   - 其余都是idea问题，强烈建议在idea通过new project的方式，然后输入GitHub上的项目地址链接进行克隆。
2. 找不到配置文件？
   - 教程中的图片是有目录信息的，src/main/recourse/application.yml中
   - 找不到WxpushApplication.java，也是仔细看教程的图，是有路径信息的。
3. 获取token失败？
   - 如果你只动了配置文件，没有改代码，100%是你appid和secretid配置错了，不要觉得自己没错，自己检查每一个字母再来质疑。
# wx-push
