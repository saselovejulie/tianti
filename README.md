# 天梯（tianti）

  天梯简介：<br>
  
    1、天梯是一款使用Java编写的免费的轻量级CMS系统，目前提供了从后台管理到前端展现的整体解决方案。
    2、用户可以不编写一句代码，就制作出一个默认风格的CMS站点。
    3、前端页面自适应，支持PC和H5端，采用前后端分离的机制实现。后端支持天梯蓝和天梯红换肤功能。
    4、项目技术分层明显，用户可以根据自己的业务模块进行相应地扩展，很方便二次开发。
    5、如果您在使用过程中遇到问题，可以通过以下方式进行互动：
       5.1、天梯官方交流群：422039518，欢迎加入，获取更多咨询服务。      
       5.2、也可以微信扫描下面二维码，留言注明：天梯+个人qq号。我会第一时间拉入群。
    6、针对入群的用户，我们将优先为您提供一对一的咨询解答服务，也可以加我微信（zhexuzhe）详聊，注明天梯用户、留下联系方式。
    7、天梯的版权属于开源作者，如果有需要对天梯进行二次开发的培训服务可以加我微信（zhexuzhe）详聊，注明天梯用户、留下联系方式。
  ![image](https://raw.githubusercontent.com/xujeff/tianti/master/screenshots/tianti_dashang_erweima.png)  <br>
   
  
  技术架构：<br>
  
     1、技术选型：Spring Data JPA、Hibernate、Shiro、 Spring MVC、Layer、Mysql等。
     2、项目结构：
       2.1、tianti-common：系统基础服务抽象，包括entity、dao和service的基础抽象；
       2.2、tianti-org：用户权限模块服务实现；
       2.3、tianti-cms:资讯类模块服务实现；
       2.4、tianti-module-admin：天梯后台web项目实现；
       2.5、tianti-module-interface：天梯接口项目实现；
       2.6、tianti-module-gateway：天梯前端自适应项目实现（是一个静态项目，调用tianti-module-interface获取数据）；
     3、使用说明：
      3.0、本项目JDK默认显示的是1.7，用户可以自行选择1.7+。
      3.1、数据库使用mysql，初始化脚本位于tianti-module-admin中的src/main/webapp/scripts/tianti_stage.sql。
      3.2、后台的登陆路径为http://ip:端口/login,用户名为admin，初始密码为123456。
      3.3、后台中所用到的图标是从font文件夹里面选择copy进去的，font文件夹在聊天群里面拥有。
      3.4、编辑器的配置修改editor_config.js的var context_ = "http://127.0.0.1:8080/tianti-module-admin";
      3.5、前端项目（tianti-module-gateway）是一个静态项目，可以直接部署到web容器，支持多端自适应，需要跑接口系统。
      3.6、采用前后端分离机制获取数据，在/src/main/webapp/static/js/config.js文件里分别配置接口地址和后台项目地址;
      3.7、前台项目可以直接部署到Nginx访问，也可以跑tianti-module-gateway应用。
      3.8、如果是tomcat跑前端应用，访问路径为http://ip:端口/tianti-module-gateway/tianti/index/index.html。
      
  ![image](https://raw.githubusercontent.com/xujeff/tianti/master/screenshots/tiantiframework.png)   
  
  前端项目概览：<br>
     PC：<br>
     ![image](https://raw.githubusercontent.com/xujeff/tianti/master/screenshots/gateway/index.png)  
     ![image](https://raw.githubusercontent.com/xujeff/tianti/master/screenshots/gateway/columnlist.png)  
     ![image](https://raw.githubusercontent.com/xujeff/tianti/master/screenshots/gateway/detail.png)  
     H5:<br>
     ![image](https://raw.githubusercontent.com/xujeff/tianti/master/screenshots/gateway/h5/index.png)  
     ![image](https://raw.githubusercontent.com/xujeff/tianti/master/screenshots/gateway/h5/columnlist.png)  
     ![image](https://raw.githubusercontent.com/xujeff/tianti/master/screenshots/gateway/h5/detail.png)  
 <br>
  后台项目概览：<br>
     天梯登陆页面：
    ![image](https://raw.githubusercontent.com/xujeff/tianti/master/screenshots/login.png)  
     天梯蓝风格（默认）：
    ![image](https://raw.githubusercontent.com/xujeff/tianti/master/screenshots/userlist.png)
    ![image](https://raw.githubusercontent.com/xujeff/tianti/master/screenshots/rolelist.png)
    ![image](https://raw.githubusercontent.com/xujeff/tianti/master/screenshots/menulist.png)                                           
    ![image](https://raw.githubusercontent.com/xujeff/tianti/master/screenshots/roleset.png)
    ![image](https://raw.githubusercontent.com/xujeff/tianti/master/screenshots/updatePwd.png)
    ![image](https://raw.githubusercontent.com/xujeff/tianti/master/screenshots/skin.png)
    ![image](https://raw.githubusercontent.com/xujeff/tianti/master/screenshots/lanmulist.png)
    ![image](https://raw.githubusercontent.com/xujeff/tianti/master/screenshots/addlanmu.png)
    ![image](https://raw.githubusercontent.com/xujeff/tianti/master/screenshots/articlelist.png)
    ![image](https://raw.githubusercontent.com/xujeff/tianti/master/screenshots/addarticle.png)  
   天梯红风格：
    ![image](https://raw.githubusercontent.com/xujeff/tianti/master/screenshots/red/userlist.png)
    ![image](https://raw.githubusercontent.com/xujeff/tianti/master/screenshots/red/rolelist.png)
    ![image](https://raw.githubusercontent.com/xujeff/tianti/master/screenshots/red/menulist.png)                                       
    ![image](https://raw.githubusercontent.com/xujeff/tianti/master/screenshots/red/roleSet.png)
    ![image](https://raw.githubusercontent.com/xujeff/tianti/master/screenshots/red/updatePwd.png)
    ![image](https://raw.githubusercontent.com/xujeff/tianti/master/screenshots/red/skin.png) 
    ![image](https://raw.githubusercontent.com/xujeff/tianti/master/screenshots/red/lanmulist.png)
    ![image](https://raw.githubusercontent.com/xujeff/tianti/master/screenshots/red/addlanmu.png)
    ![image](https://raw.githubusercontent.com/xujeff/tianti/master/screenshots/red/articlelist.png)
    ![image](https://raw.githubusercontent.com/xujeff/tianti/master/screenshots/red/addarticle.png)  
    ![image](https://raw.githubusercontent.com/xujeff/tianti/master/screenshots/tianti_dashang_erweima.png)  
    
    
