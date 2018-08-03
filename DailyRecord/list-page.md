## 任务介绍

**简介：**护工列表页-一个常见的移动页面，需要使用bootstrap

**要求：**  

- 解决垂直居中；
- 模拟下拉选框；
- 做出复杂的列表页；

**任务原型：**

![](http://jns.img.bucket.ks3-cn-beijing.ksyun.com/skill/daily/8d48b632-affb-4018-b0ab-b119c5180a6f.png) 

**验收标准：**

- 顶部底部固定在屏幕上方下方
- 自适应布局，在主流手机中都可以显示
- 当屏幕过小时，表格内容大小能根据屏幕改变。
- 以bootstrap作为基础布局，添加自定义样式表对bootstrap无法表达的细节样式进行调整   

**完成步骤：**     

1. 整体布局    

   ![5](C:\Users\MaiBenBen\Desktop\5.png)  

2. **编码过程：**  

- 

## 完成的事情  

- 掌握了css雪碧图的使用
- 完成了一部分任务六代码编写
- 懂得了如何使用bootstrap
- 了解了栅栏布局
- 完成部分页面的编写  

***

## 遇到的问题

1. 不知道css雪碧图如何使用
2. bootstrap组件使用的过程中发现和预设的不一样

## 收获

1. #### **bootstrap介绍和应用**          

- 一款简洁，直观，强悍的前端开发框架，让web开发更迅速，简单。  

- 准备：  
  - 先要去它的官网[http://v3.bootcss.com](http://v3.bootcss.com/)进行下载：  
    1. 下载Bootstrap->用于生产环境的Bootstrap  
    2. 下载成功后可以得到一个.zip的文件，解压后我们可以得到一个包含css、fonts和js的文件夹，准备工作我们就做好了，然后新建一个文件夹，重命名后，将刚刚三个文件夹复制到该文件夹中，再用自己的编辑器打开刚刚的文件夹，点击file-open folder，选择该文件夹点击确定即可。最后在该文件夹下新建一个index.html文件
    3.  重新回到bootstrap官网，导航栏选择“起步”，向下拖动或在右侧选择“基本模板”，将下列代码进行复制，粘贴到index.html中 。  

  - 用法： 

    - 链接下面这两个基础文件

       <link rel="stylesheet" href="../bootstrap/css/bootstrap.min.css">
         <link rel="stylesheet" href="../bootstrap/css/bootstrap-theme.min.css">

    - 根据自己的需要在里面添加相应的组件即可

    ![1533215047280](C:\Users\MAIBEN~1\AppData\Local\Temp\1533215047280.png)

    - 在body内添加相应的组件内容，就能实现想要的效果，然后再进行修改

    ![](http://jns.img.bucket.ks3-cn-beijing.ksyun.com/skill/daily/80c92624-e36c-44b7-b6e5-5ff7d6333a91.png)  

    ![](http://jns.img.bucket.ks3-cn-beijing.ksyun.com/skill/daily/da7c45fd-fd10-488b-8a02-d37c1e71a7a1.png)

- 注意事项：

  - bootstrap里面自带的组件不要轻易修改，要修改的话，自己创建一个类进行修改。

- 参考： 

  - https://www.w3schools.com/bootstrap4/bootstrap_get_started.asp  
  - http://www.bootcss.com/   
  - https://blog.csdn.net/gaiyindexingqiu/article/details/72454069

2. #### **深刻理解flexbox**    

![](http://jns.img.bucket.ks3-cn-beijing.ksyun.com/skill/daily/3e59d0ca-0694-4a32-8232-74e3eed31d03.jpeg)  

- **flexbox简介：**

  - Flexbox模块即使不知道视窗大小或者未知元素情况之下都可以智能的，灵活的调整和分配元素和空间两者之关的关系。简单的理解，就是可以自动调整，计算元素在容器空间中的大小。      

- **基础应用：**  

  - 使用一个无序列表(`ul`)和一群列表元素(`li`)，启动Flexbox格式化上下文的方式如下： 

  ```html
  /* 声明父元素为flex容器 */
  ul {
      display:flex; /*或者 inline-flex*/
  }
  ```

  给列表元素(`li`)添加一点基本样式，这里你可以看到发生了什么。

  ```css
  li {
      width: 100px;
      height: 100px;
      background-color: #8cacea;
      margin: 8px;
  }
  ```

  ![](http://jns.img.bucket.ks3-cn-beijing.ksyun.com/skill/daily/898ceeff-a558-454d-9fe3-2d8c6ea51b50.png)  

  通过图片可以看出，本该遵循css垂直堆栈的ul块状元素，从上往下排，用了flexbox布局之后，却在一行上显示，变成了水平显示，就像使用了float一样。    

- **意混淆的属性：**

  - **flex-flow：flex-direction  flex-wrap；** ![](http://jns.img.bucket.ks3-cn-beijing.ksyun.com/skill/daily/a03bb20f-488e-4ab5-aafc-8d04f7cd0006.jpeg)
  - **justify-content: space-between;**   
    - 让除了第一个和最后一个Flex项目的两者间间距相同（两端对齐）  

  ![](http://jns.img.bucket.ks3-cn-beijing.ksyun.com/skill/daily/594a4438-8792-4e0e-8e50-4f3c78eb5118.jpeg)  

  - **justify-content：space-around;**   
    - 让每个Flex项目具有相同的空间  ,和space-between不同的是，第一个Flex项目和最后一个Flex项目距Main-Axis开始边缘和结束边缘的的间距是其他相邻Flex项目间距的一半 。

  ![](http://jns.img.bucket.ks3-cn-beijing.ksyun.com/skill/daily/3b061e00-5fbb-41c1-881f-d7e00bc9df57.png)    

  - **align-items: stretch(默认值);**      让所有项目高度和Flex容器高度一样    

    ![](http://jns.img.bucket.ks3-cn-beijing.ksyun.com/skill/daily/22ec14ae-7323-4daa-ac10-07814213ae13.png)   

  - order：integer;   按数字大小从低往高排列。  

  - **flex-grow: 0(默认)；和flex-shrink: 1(默认)；**  

    - 控制flex项目在容器有多余空间如何放大，在没有额外空间又如何缩小。可以接受0或大于0的任何数  
    - 默认情况下，`flex-grow`属性值设置为`0`。表示Flex项目不会增长，填充Flex容器可用空间。取值为`0`就是一个开和关的按钮。表示`flex-grow`开关是关闭的。

    ![](http://jns.img.bucket.ks3-cn-beijing.ksyun.com/skill/daily/b755ce45-0ca1-4f54-b45f-e49200bc47e5.png)  

    -  如果把`flex-grow`的值设置为`1`。  现在Flex项目扩展了，占据了Flex容器所有可用空间。也就是说开关打开了。如果你试着调整你浏览器的大小，Flex项目也会缩小，以适应新的屏幕宽度。 

    ![](http://jns.img.bucket.ks3-cn-beijing.ksyun.com/skill/daily/16ef3f99-f2a0-4dbd-b2cb-5c6b9630c121.png)    

  - **flex-basis**   

    - `flex-basis`属性可以指定Flex项目的初始大小。也就是`flex-grow`和`flex-shrink`属性调整它的大小以适应Flex容器之前。   

    - `flex-basis`默认的值是`auto`。`flex-basis`可以取任何用于`width`属性的任何值。比如 `% || em || rem || px`等。   

    - 如果`flex-basis`属性的值是`0`时，也需要使用单位。即`flex-basis: 0px`不能写成`flex-basis:0`。   

    - 默认情况，Flex项目的初始宽度由`flex-basis`的默认值决定，即：`flex-basis: auto`。Flex项目宽度的计算是基于内容的多少来自动计算，意味着，如果你增加Flex项目中的内容，它可以自动调整大小 。

    - 如果你想将Flex项目设置一个固定的宽度，你也可以这样做：

      ```
      li {
          flex-basis: 150px;
      }
      ```

      现在Flex项目的宽度受到了限制，它的宽度是`150px`。

      ![img](http://jns.img.bucket.ks3-cn-beijing.ksyun.com/skill/daily/9a7ebec6-deeb-455c-9952-8fded7d8908a.png)  

    - `flex`是`flex-grow`、`flex-shrink`和`flex-basis`三个属性的速记（简写）GSB 。   

  - **flex: 0 0 auto;** 

    - 相当于`flex: none`。 宽度是被自动计算，不过弹性项目不会伸展或者收缩（因为二者都被设置为零）。伸展和收缩开关都被关掉了.试着缩放一下浏览器，你会注意到弹性项目不会收缩其宽度。它们从父元素中突出来了，要看到所有内容，   必须横向滚动浏览器 .  

  ![img](http://jns.img.bucket.ks3-cn-beijing.ksyun.com/skill/daily/2f9fb024-14ae-4dc8-a930-44eaf29d80ea.png)   

  ![img](http://jns.img.bucket.ks3-cn-beijing.ksyun.com/skill/daily/d34910cb-78d0-4370-ab85-0fd7c388f33c.png)

  - **flex: “positive number”**

    - 这里正数可以代表任何正数（没有引号）。这与 `flex: “正数” 1 0` 相同。

    ​    `flex: 2 1 0` 与写为 `flex: 2` 是一样的，`2`表示任何正数。    

  - **flex: auto; 等同于flex： 1 1 auto；**    

  - **参考：**

    - https://www.w3.org/TR/css-flexbox-1/    
    - https://hufan-akari.github.io/solved-by-flexbox/    
    - https://blog.csdn.net/nishiwodebocai21/article/details/81319830  
    - A Friendly Introduction to Flexbox for Beginners

3. #### 雪碧图的制作和使用  

   - 参考：  

     - https://www.zhihu.com/question/19850818     
     - https://www.w3schools.com/css/css_image_sprites.asp  
     - https://developer.mozilla.org/en-US/docs/Web/CSS/clip-path

   - 雪碧图介绍：  

     ![1533202491812](C:\Users\MAIBEN~1\AppData\Local\Temp\1533202491812.png)

   - 制作：[CSS Sprites Generator](https://www.toptal.com/developers/css/sprite-generator)，在线自动制作工具.也可以使用ps进行制作  

   - 实现原理： 通过background-position对背景图进行定位，控制一个层，可显示的区域范围大小，通过一个窗口，进行背景图的滑动。  

     ![1533206965127](C:\Users\MAIBEN~1\AppData\Local\Temp\1533206965127.png)  

     

   - 使用：  

     - ！！！！

   - 应用场景：

     - ！！！！   

4. #### background-position详解  

   - > - 属性值为百分比时，将以图片的 **中心点** 为基准计算其相对位置。
     >
     >   - W3C怎么说：
     >
     >     ```
     >         With a value pair of '0% 0%', the upper left corner of the image is aligned with the upper left corner of the box's. A value pair of '100% 100%' places the lower right corner of the image in the lower right corner of padding area. With a value pair of '14% 84%', the point 14% across and 84% down the image is to be placed at the point 14% across and 84% down the padding area.
     >         
     >          1、background-position: 0% 0%;图像的左上角和父级的左上角对齐
     >          2、background-position: 100% 100%;图像的右下角和父级的右下角对齐
     >          3、background-position: 14% 84%;图像的中心点14% 84%。将被放置在父级的14% 84%的位置
     >         总结1：也就是说如果用百分比来作为 background-position的属性值的话,那么背景图片相对于容器的中心点事随时都在改变的。
     >         总计2：background-position: 10% 20%; 背景图片首先会把自身的中心点移动到10% 20%的位置。然后在根据父级元素的宽高来移动(10% 20%)
     >     ```

     
     

     > - 属性值为像素时，始终以图片的 **左上角** 为基准。

     参考：http://linxz.github.io/blog/css%E5%B1%9E%E6%80%A7%E5%9F%BA%E7%A1%80/2015/09/talk-about-background-position-values.html

     **例子**

     ```
     /*
     1、当前图片宽高为(200*200);
     2、当前元素大小为(100*100);
     图片的原中心点是(0, 0)
     现在的中心点位置是(200*10%, 200*20%),也就是(20px, 40px)。
     按照之前的推理：
     1、图片以(20px,40px)为中心点,移动元素宽度的10%,元素高度的20%,也就是移动了(10px,20px);
     2、最终移动的距离是：(-20px+10px,-40px+20px) === (-10px,-20px);
     */
     .box{
       	width: 100px;
       	height: 100px;
       	background: url(demo.png) no-repeat;// 当前图片宽高为200*200
       	background-position: 10% 20%;
     }
     ```

     **公式计算**

     > 根据如上的推理,我们若想得到定位的百分比值,
     >
     > 我们需要元素的宽高 `(eleWidth,eleHeight)` ,图片的宽高 (`imgWidth,imgHeight`) ,当前图片移动后的坐标 `imgX,imgY`
     >
     > - left: `-imgX/(eleWidth-imgWidth)*100%;`
     > - top:`-imgY/(eleHeight-imgHeight)*100%;`

     **使用**

     参考：http://www.jianshu.com/p/d3b19968a4c2

     ```
     //$spriteWidth 雪碧图的宽度px
     //$spriteHeight 雪碧图的高度px
     //$iconWidth 需要显示icon的宽度px
     //$iconHeight 需要显示icon的高度px
     //$iconX icon的原始x坐标
     //$iconY icon的原始y坐标
     //
     @mixin bgPosition($spriteWidth, $spriteHeight, $iconWidth, $iconHeight, $iconX, $iconY){
     
         background-position: (($iconX / ($spriteWidth - $iconWidth)) * 100% ($iconY / ($spriteHeight - $iconHeight)) * 100%);
     }
     
     .icon2{
         width: 0.74rem;
         height: 0.64rem;
         @include bgPosition(1072, 442, 74, 64, 188, 5);
     }
     ```

     

## 深度思考

1. 为什么设置了flex布局后，子元素的float，clear，还有vertical-align属性不起作用？

2. flex项目上使用margin：auto对齐会出现什么情况？

   - 当在Flex项目上使用 `margin: auto` 时，值为 `auto` 的方向（左、右或者二者都是）会占据所有剩余空间。 举例子说明一下：

     ```
     <ul>
         <li>Branding</li>
         <li>Home</li>
         <li>Services</li>
         <li>About</li>
         <li>Contact</li>
     </ul>
     
     ul {
         display: flex;
     }
     li {
         flex: 0 0 auto;
     }
     ```

     你可以看到如下的效果：

     ![img](http://jns.img.bucket.ks3-cn-beijing.ksyun.com/skill/daily/dba88504-9946-45e9-bb50-6fc71f021868.png)

     这里有几件事情要注意：

     - `flex-grow` 值为设置为`0`。这就解释了为什么列表项不会伸展。
     - Flex项目向Main-Axis的开头对齐（这是默认行为）。
     - 由于项目被对齐到Main-Axis开头，右边就有一些多余的空间。看到了吧？

     ![img](http://jns.img.bucket.ks3-cn-beijing.ksyun.com/skill/daily/c8e8b104-3d41-4ee0-ba0c-b05c56187026.png)

     现在在第一个列表项（branding）上使用 `margin: auto`，看看会出啥情况。

     ```
     li:nth-child(1) {
         margin-right: auto; /*只应用到右外边距*/
     }
     ```

     ![img](http://jns.img.bucket.ks3-cn-beijing.ksyun.com/skill/daily/5296c734-61b3-4c2a-81b0-32c474734da0.png)

     刚刚发生了什么？之前的剩余空间现在已经被分配到第一个Flex项目的右边了。

     ![img](http://jns.img.bucket.ks3-cn-beijing.ksyun.com/skill/daily/29540afc-7610-4bab-a7a4-f20e304b2830.png)

     **当在Flex项目上使用 margin: auto 时，值为 auto 的方向（左、右或者二者都是）会占据所有剩余空间**。http://jns.img.bucket.ks3-cn-beijing.ksyun.com/skill/daily/29540afc-7610-4bab-a7a4-f20e304b2830.png

     如果想让一个Flex项目的两边都用自动外边距对齐，该怎么办呢？

     ```
     /* 如果愿意的话，也可以用 margin 简写来设置两个边 */
     li:nth-child(1) {
         margin-left: auto;
         margin-right: auto
     }
     ```

     ![img](http://jns.img.bucket.ks3-cn-beijing.ksyun.com/skill/daily/fa78b780-69d9-44f4-a151-cca278c0832f.png)

     现在空白被分配到Flex项目的两边了。

     那么，这是不是对很酷的自动外边距对齐的一种折衷方案呢？看起来是。如果没注意的话，它也可能是受挫之源。当在一个Flex项目上使用自动外边距（`margin: auto`）时，`justify-content` 属性就不起作用了。

     例如，在上面的Flex容器上通过 `justify-content`属性，设置不同的对齐选项时，对布局没有影响。

     ```
     ul {
         justify-content: flex-end;
     }
     ```

     ![img](http://jns.img.bucket.ks3-cn-beijing.ksyun.com/skill/daily/6d83f616-5a0e-4c68-b4c4-854e92dd6365.png)    

3. flex是否兼容所有浏览器？  

   - [Flexbox规范](http://dev.w3.org/csswg/css-flexbox/)还没有最终确定，所以自然会有一些最新的草案和浏览器实现滞后现象  
   - 可以阅读https://github.com/philipwalton/flexbugs    

4. flex的项目可以成为flex容器么？  

   - 答案是可以的，并且你想嵌套多深就嵌套多深（不过理智的做法是保持一个合理的水平）   

5. flex布局是否自带padding？  

6. css雪碧图是否支持img图片导入？

   - 不支持img图片导入，只适用于background-img背景图片的定位。

7. css雪碧图如何自适应不同屏幕？

   - 在rem布局下使用雪碧图，  结合background-size，在处理sprite图片时，我们只能给background-size取具体值。那么这个值取多少呢？其实只要写我们切出来的图片的实际尺寸就行。 

   - 假如我们要把图标缩小到原来的一半的话可以按照下面的方式来做：

     ```html
     <!DOCTYPE html>
     <html>
     <head lang="en">
         <meta charset="UTF-8">
         <title></title>
         <style>
             .img{width:44px;height:30px;background:url("image/sprite.png") 0 -20px no-repeat;}
             .img1{width:22px;height:15px;background:url("image/sprite.png") 0 -10px no-repeat; background-size:22px auto;}
         </style>
     </head>
     <body>
     <div class="img"></div>
     <div class="img1"></div>
     </body>
     </html>
     ```

   - 参考：http://web.jobbole.com/87652/

8. rem布局的真正含义是什么？  

   - 所谓rem布局就是指为文档的根节点<html>元素设置一个基准字体大小，然后所有的元素尺寸都以rem为单位来写。比如将<html>的字体设为100px，如果需要做一个100*200的元素，css如是写：

     div{   width: 1rem;    height: 2rem;}

     那么最终得到的元素宽高就是100*200px了。 

## 明日计划

- [ ] 完成任务六所有代码编写
- [ ] 解决css雪碧图不能准确定位以及自适应页面
- [ ] 深度思考任务过程遇到的所有问题
- [ ] 完成任务六后想想怎么用bootstrap进行页面的快速重构
- [ ] 日报编写