
## 完成的事情      

1. **完成了任务五** 

2. **学习了css编码规范[css编码规范](https://github.com/fex-team/styleguide/blob/master/css.md),并且按照编码规范对自己的代码进行了优化**  

3. **应用flex进行网页布局**

4. **了解了css通配符&选择器性能优化/浏览器渲染原理**

   ***

   

   ## 遇到的问题    

   1. 导航栏布局两栏布局不知道如何用flex进行布局   
      - 解决方案  :  在container内部定义三个部分（最后一个定义一个空标签），然后用flex：1；水平均分为3部分，中间的文字用text-align:center；水平居中对齐。  
   2. 背景图片不知道如何全屏显示，且在拉伸和压缩情况下图片不会变形    
      - 解决方案：让背景图片不平铺，且让background-size：100% 100%;  
   3. 图片怎么自适应大小  
      - 解决方案：设置图片的宽高，然后使用标签max-width： xrem;保证图片不超过背景。  
   4. 文字不能完全显示在按钮上方  
      - 解决方案：父级元素设置margin-bottom即可  
   5. 自我介绍内容不能自适应屏幕适中显示  
      - 解决方案：在父元素上使用align-items: center;即可。

   

   

   ## 收获 

   

   ###  1. css通配符的弊端       

   - 观点：  
     - 查询次数多&匹配效率低，会影响性能但是影响不大
     - 影响可维护性 & 容易造成样式冲突
     - 所有需要设置的元素放在一起设置
     - 建议使用css reset文件
       - [necolas/normalize.css](https://github.com/necolas/normalize.css)
       - [jgthms/minireset.css](https://github.com/jgthms/minireset.css) 

   1. 选择器性能优化 参考：[网站CSS选择器性能讨论](http://www.aliued.cn/2013/01/24/%E7%BD%91%E7%AB%99css%E9%80%89%E6%8B%A9%E5%99%A8%E6%80%A7%E8%83%BD%E8%AE%A8%E8%AE%BA.html)

   2. 样式系统从最右的选择符开始向左进行匹配规则，只要左边还有选择符就会继续向左移动.

   3. CSS选择器效率排序(快到慢)：

      - id选择器（#myid）
      - 类选择器（.myclassname）
      - 标签选择器（div,h1,p）
      - 相邻选择器（h1+p）
      - 子选择器（ul < li）
      - 后代选择器（li a）
      - 通配符选择器（*）
      - 属性选择器（a[rel=”external”]）
      - 伪类选择器（a:hover,li:nth-child）

   4. 优化方法：

      - id选择器最快，不要同时使用其他选择器
      - 类选择器尽量不合标签选择器同时用
      - 明确DOM结构情况下优先使用子选择器
      - 使用类选择器替代后代选择器&子选择器
      - 尽量用继承避免编写重复样式       

      

      ### 2.title与h1、b与strong、i与em、img的alt与title、src与href有什么区别 

      - 参考：[Web品质](http://www.w3school.com.cn/quality/quality_elements.asp)

      - <title> & <h1>: <title>用于描述网页内容且整个文档中只出现一次，在搜索引擎列表、窗口标题栏、用户书签中可见，应尽量短且具有描述性; <h1>用于描述网页中最顶层的标题,符合语义化;
      - <b> & <strong>: <b>为无意义的加粗，现在的Web标准不建议直接元素设计具体表现形式,故建议少用; <strong>表更强的强调，可以用CSS替换其加粗样式，比较符合Web标准;
      - <i> & <em>: <i>为无意义的斜体，现在的Web标准不建议直接元素设计具体表现形式,故建议少用; <em>表示一般强调，可以用CSS替换其斜体样式，比较符合Web标准;
      - <img>的alt & title属性、src & href属性：
        - alt：无法显示图片时起到文本替代的作用, 浏览器在特殊浏览器上有辅助作用;
        - title: 鼠标划过时的文本提示;
        - src：资源对应路径，将资源加载到文档中;
        - href：指向的链接，不加载资源;  

   ### 3.background学习

   - 定义：用于定义HTML元素的背景.
   - 属性：
     - background-color: 背景色
       - 设定方式：
         - 十六进制： #ff0000 （推荐使用符合css代码规范）
         - RGB: rgb(255, 0, 0)
         - 颜色名称: red
         - RGBA(???)
         - 透明：transparent
         - inherit：继承父元素背景色
     - background-image: 背景图像(默认平铺重复)
       - 设定方式： url('[path]')
     - background-repeat:
       - 水平平铺：repeat-x
       - 垂直平铺: repeat-y
       - 不平铺：no-repeat
     - background-attachment：是否随页面滚动
       - scroll: 跟随页面滚动
       - fixed：跟随进度条位置
       - inherit: 继承自父元素
     - background-position: 设置背景图像的起始位置(Firefox和Opera需要先设置为fixed才能正常工作)
       - 设定方式：
         - top|center|bottom(垂直) left|center|right(水平)
         - x%(水平) y%(垂直)
         - xpos(水平) ypos(垂直)
     - background-origin: 相对位置
       - 值：padding-box|border-box|content-box
     - background-size: 背景图片大小
       - 值： length(宽度,高度)|percentage(宽度,高度)|cover(保持纵横比并缩放成*完全覆盖*背景定位区域的最大大小)|contain(保持纵横比并缩放成*合适*背景定位区域的最大大小，即只满足短的方向的等比例缩放)  

   ### 4.rem, px, vw, vh, em实际应用

- 元素**严格不可缩放**时，使用px
- 一切可扩展都应该用rem, 包括媒体查询
- 千万不要用em控制字体的大小
- em用于缩放一些没有默认字体大小的元素，当字体变大整个组件也能随之变大
- 多列布局用%较好
- vw、vh、vm做页面排版很厉害，但是**兼容做得比较晚**，所以优先还是用rem和%解决问题



### 深度思考  

***

 

### 1. CSS3的Flexbox（弹性盒布局模型）以及适用场景

- Flex布局用于简洁、完整、响应式地实现各种页面布局，给盒模型提供最大的灵活性. 采用Flex布局的元素称为Flex容器(flex container), 其所有子元素自动成为容器成员即Flex项目(flex item). 容器默认存在两根轴，水平的主轴(main axis)和交叉轴(cross axis),Flex项目默认沿主轴排列.
- 适用场景：
  - 网格布局：设置flex
  - 百分比布局：先设置flex:1, 再设置flex: 0 0 %
  - 圣杯布局: 该填满的用flex:1
  - 输入框布局：一侧定长，其他flex:1填满
  - 悬挂式布局：一侧定长，其他flex:1填满
  - 固定底栏：方向column，定高

### 2.如何理解vertical-align与line-height？

- 参考：
  - [深入理解line-height与vertical-align](http://www.cnblogs.com/xiaohuochai/p/5271217.html)
  - [CSS深入理解vertical-align和line-height的基友关系](http://www.zhangxinxu.com/wordpress/2015/08/css-deep-understand-vertical-align-and-line-height/)
- line-height: 行高.只影响inline元素及内容.
  - 可选值：<length>|<percentage>|<number>|normal|inherit
  - 默认值：normal(通常是font-size的1.2倍)
  - 内容区：行内文本，font-size决定了其高度;
  - 行内框：等于行间距(上半)+内容区+行间距(下半)，line-height决定了其高度;当font-size>line-height时行内框小于内容区;
  - 行框：行内的最高行内框顶端到最低行内款底端的距离,且各行框顶端挨着上一行框的底端;
  - 框属性：
    - padding、border、margin的top&bottom都不影响行高（行框高度）, 其left&right都会应用到元素的开始结尾;
    - 行内元素的边框边界由font-size控制而非line-height;
  - 行内替换元素：根据元素的标签属性来决定其显示的具体内容的元素，如<img> & <input>. 其位于基线(vertical-align:bashline)上, 替换元素的基线是正常流中最后一个行框的基线，除非元素内容为空或者本身的overflow属性值不是visible，这种情况下基线是marigin底边缘.
- vertical-align
  - 可选值：
    - 关键字值： baseline|sub|super|text-top|text-bottom|middle|top|bottom
    - 长度值：??em|??px
    - 百分比值：?% (*vertical-align的百分比相对于line-height进行计算*)
    - 全局值：inherit|initial|unset
  - 默认值：baseline
- 关系
  - *对于内联元素各种想得通或者想不通的行为表现，基本上都可以用vertical-align和line-height来解释，以及进行行为矫正*
  - vertical-align的百分比相对于line-height进行计算
- [学习演示地址](http://118.89.44.244/cssup/study/verticalAlignandlineHeight.html)      

### 3.css可以绘制哪些常见的特殊形状？

- 参考：
  - [奇妙的 CSS shapes(CSS图形)](http://www.cnblogs.com/coco1s/p/6992177.html)
  - [The Shapes of CSS](https://css-tricks.com/examples/ShapesOfCSS/)
- 梯形、三角形、六边形、圆形、心型、五角星...     

## 计划完成的事  

***

1. **了解并运用bootstrap布局**  

2. **掌握css sprites雪碧图的用法**  

3. **制作雪碧图**  

4. **完成日报内容**  

5. **做深度思考**  

   