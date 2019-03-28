# css笔记

# css简介 





1**.css：层叠样式表**   英文全名：cascading style sheets

**用来修饰HTML等样式文件的计算机语言**

2.css 语法

![1552726250714](C:\Users\ADMINI~1\AppData\Local\Temp\1552726250714.png)

3.样式的创建（内部样式表 外部样式表 内联样式表）

A. **内部样式表**

<style>.......</style>

写在标记<head></head>中。

B.**外部样式**

**外部样式的创建**

<link rel="stylesheet" type="text/css"  href="目标文件的路径及文件名称”

**外部样式标的导入**

<style>

@import url(目标文件的路径及文件名全称)

</style>

C.**内联样式（行间样式，行内样式，嵌入式样式，内嵌样式）**

<标签 style=“属性：属性值；属性：属性值；”>  </标签>

例子：<div style="width:500px;  height:200px;"> </div>

4.**样式表的优先级**

a. **内联**样式表的优先级**最高**

b.内部样式表与外部样式表的优先级和书写顺序有关，**后书写的优先级最高**

c.作用域：**内联样式的作用域最小**，只能用于当前元素，其次是内部样式表，能应用于当前HTML文件，最后是内部样式表，能应用于所有链接的HTML文件。

**id选择器 **

**只定义页面中某个唯一的元素对象 ，最大用处：创建网页的外围结构**

5. **伪类选择器**

   a:link{属性：属性值;}超链接的初始状态; 

   a:visited{属性：属性值;}超链接被访问后的状态; 

   a:hover{属性：属性值;}鼠标悬停，即鼠标划过超链接时的状态; 

   a:active{属性：属性值;}超链接被激活时的状态，即鼠标按下时超链接的状态; 

   **Link--visited--hover--active。** 必须按顺序写

   **a:link,  a:visited,  a:hover,   a:active** 

   # css文本属性

   

   1、**文本大小：**

   **{font-size:12px;}**    单位还可以是em，是父级元素的font-size的倍数；   /系统默认的字号大小为16px 

   2、**文本字体：**

   **{font-family:字体1，字体2，字体3；}** 

   3、**文本颜色：**

   **{color:颜色值;}**red/#f00/rgb(255,0,0) 

   4、**文字加粗font-weight:bolder**     (更粗的)/bold   （加粗）/normal    （常规）/100—900; 

   5**、文本倾斜：**

   **font-style：italic**（倾斜字体）/oblique（让现有字体发生倾斜）/normal（常规显示）; 

   6**、水平对齐方式**

   **{text-align:left**左/right右/center居中/justify两端对齐(在部分浏览器中，对于中文不起作用);}      只针对文本或图片

   7、**垂直对齐方式**

    **{vertical-align:**top上/bottom下/middle居中/baseline基线（某些特定的元素类型起作用）;}

   

   8、**文字行高** 

   **{line-height:normal/value;}**

   **line-height:20px;** line-height:2em; (当行高的单位省略时，默认为em)

   *当单行文本的行高等于容器高时，可实现单行文本在容器中垂直方向居中对齐； *

   *当单行文本的行高小于容器高时，可实现单行文本在容器中垂直中齐以上； *

   *当单行文本的行高大于容器高时，可实现单行文本在容器中垂直中齐以下（IE6及以下版本存在浏览器兼容问题）* 

   9、**文本修饰** 

   **text-decoration:none**（没有修饰）/underline（添加下划线）/overline（添加上划线）/line-through（添加删除线）

    10、**首行缩进：{text-indent:value;}**   *只对第一行起作用*

   11、**检索英文字母大小写{text-transform:**none无转换/capitalize首字母大写/uppercase全都大写/lowercase全都小写;}。 

12、**字间距{letter-spacing:value;}**控制英文字母或汉字的字距。

13、**词间距{word-spacing:value;}**控制英文单词词距。

扩展：14、**文本流控制{layout-flow:horizontal/vertical-ideographic;}**

**说明：**

1）**horizontal:自左向右**

**2）vertical-ideographic:自上而下**

15、文字属性简写：font:bolder italic 12px/1.5em "宋体";     简写时，字体和字号是必备 

font属性的简写：字号，行高，字体 

说明:font的属性值应按以下次序书写(各个属性之间用空格隔开) 顺序: font-style font-weight font-size / line-height font-family 

# css列表属性

1、**定义列表符号样式**

**list-style-type：**disc(实心圆)/circle(空心圆)/square(实心方块)/none(去掉列表符号)；

2、**使用图片作为列表符号**

**list-style-image：url(所使用图片的路径及全称)；**

3、**定义列表符号的位置**

list-style-position:outside(外边)/inside(里边)；

***list-style:none;去掉列表符号***

# 边框的属性和属性值

border:边框宽度 边框风格 边框颜色;

例如：border:5px solid #ff0000

**边框宽度：border-width:**

**边框颜色：border-color:**

**边框样式：*border-style:**solid(实线)/dashed(虚线)dotted(点划线)double(双线)***none(去掉边框)**;

可单独设置一方向边框，

border-bottom:边框宽度 边框风格 边框颜色;      底边框

border-left:边框宽度 边框风格 边框颜色;             左边框

border-right:边框宽度 边框风格 边框颜色;          右边框

border-top:边框宽度 边框风格 边框颜色;           上边框

- # CSS背景属性

- 

- 1、**背景颜色** 

- **{background-color:**颜色值;}

- 2、**背景图片的设置** 

- **background-image：url(背景图片的路径及全称）；**

- 3、**背景图片平铺属**

- **{background-repeat**:no-repeat不平铺/repeat平铺/repeat-x  X轴平铺/repeat-y   Y轴平铺 }

- 4、**背景图的位置**

- **{background-position:**left/center/right/数值      top/center/bottom/数值;}

- 5.**背景图的固定**

- **{background-attachment:fixed固定/scroll滚动;}**

- fixed 固定，不随内容一块滚动，根据可视窗口固定位置；
  scroll:随内容一块滚动。

# css浮动属性

- *语法：**float:none/left/right;***
  浮动的目的：就是让**竖着**的元素**横着显示**

- 一个元素设置float：left/right;时，元素会脱离文档流（半脱离），不占空间；
  有三个取值：
  left:元素向左浮动
  right:元素向右浮动
  none:默认值，不浮动。

  *清除浮动可以理解为打破横向排列。*

  *清除浮动的属性是clear，语法：*

- *clear : none | left | right | both*

- *none：默认值。允许两边都可以有浮动对象*

- *left：清除左浮动/不允许左边有浮动对象*

- right  :  清除右浮动/不允许右边有浮动对象*

  both  :  清除两端浮动/不允许有浮动对象*

  *有一点是要记住的那就是*

  *对于CSS的清除浮动(clear)，一定要牢记：这个规则只能影响使用清除的元素本身，不能影响其他元素*

   **浮动**
  html网页中对于元素的种种限制，其实都来自于标准文档流，例如行内元素不能设置宽度和高度，块级元素不能并排显示等等，那么想要摆脱这些限制，那么就需要"脱离标准文档流".

  脱离标准文档流的方法有三种:
  	**浮动**
  	**绝对定位**
  	**固定定位**

  浮动的标准特性:
  	**1.让元素脱离标准文档流**
  	**2. 浮动会让元素相互紧贴**
  	**3. 会存在字围效果**
  	**4. 收缩效果**

  浮动元素带来的影响解决方案:
  	**1. 给父元素(必须是子元素发生了浮动)设置一个具体的高度**
  	**2. 使用clear:both属性** 
  	**3. 使用:after :before(伪类)来实现。**

  #盒子模型

  1. **盒子模型**


  包含五个元素

  **width 宽度   height 高度   padding内边距    border    margin 外边距**

  border:1px solid red;

  1px 表示border的宽度
  solid 线型
  red 颜色

  border-width:1px
  border-style:solid
  border-color :red

  border-top-right-bottom-left

  ```html
  div {
  	border:1px solid red;
  	border-bottom:1px solid blue;
  	border-bottom-color:blue;
  
  	border-top-width:1px 
  	border-top-style:solid
  	border-top-color:red;
  }
  ```

  **padding** 
  **padding是内容与边框之间的距离 ，我们称它为内边距。**  
  padding有四个方向，我们可以采用简写:
  padding:10px;  上右下左四个方向的padding都为10px
  padding:10px 20px; 上下10 左右20
  padding:10px 20px 30px ; 上10 左右20 下30 
  padding:10px 20px 30px 40px; 上10 右20 下30 左40

  单独某个方向设置值：
  padding-top
  padding-right
  padding-bottom
  padding-left 

  可以进行padding覆盖
  padding:10px;
  padding-left:20px;

  Tip:padding使用后会增加盒子实际所占的宽度和高度，如果不想改变盒子原本所占有的宽度和高度，那么就把宽度和高度减少(内容的宽度和高度)

  

  **标准文档流**
           所谓的文档流指的就是元素(标签)排版(浏览器解析的时候)，                        顺序是  **从上向下 从左向右**

  标准文档流微观现象：
  	**a:空白折叠**  
  	**b:高矮不齐，底边对齐**
  	**c:自动换行 一行写不满就换行写**  

  标准文档流中的元素等级问题：
  **块级元素和行内元素**

  行内元素的特性:
  	a: 没有办法设置宽度和高度，宽度和高度只能凭借内容去撑起来，如果行内元素当中没有内容的话，就会缩成一小条。
  	b: 多个行内元素可以并排显示
  块级元素的特性:
  	a: 可以设置宽度和高度
  	b: 如果一个块级元素没有设置宽度，那么这个块级元素宽度就会默认占满当前屏幕宽度的百分百。
  	c: 块级元素不能和其他元素并排显示

  *常用的块级元素标签:*
  	div p h1-h6  列表 ul li ol li dl dt dd 
  *常用的行内元素标签:*
  	*b  span em i u s a*

  **行内元素与块级元素相互转换  -- display** 
  **如果想要把行内元素转换成块级元素 display:block;**
  **如果想要把块级元素转换成行内元素  display:inline;**
  **display:inline-block; 转换成行内块元素 (特性：既可以设置宽高又可以并排显示)**

  # 选择器

  CSS如何使用
  **① style 属性 优先级最高**
  **② style 标签**
  **③link 推荐使用这种因为能够做到结构与样式分离**
  **④@import url()**

  选择器 

  **A:三种基础选择器** 
  **id 选择器  权重最高**
  **class 选择器  其次**
  **html标签选择器  最后** 

  B: **稍微高级一点的选择器:**
  **通配符选择器 * 可以使用，但是不推荐使用，主要用于测试**
  **后代选择器  div p  .d1 .d2**
  **子元素选择器 div>p;    .d1>p** 
  **交集选择器  span.s1**
  **并集选择器  span,h1,div     .d1 , .d2 ,div** 
  **序列选择器  ul li:first-child  ul li:last-child**  
  **相邻兄弟选择器 div+p**  
  **普通兄弟选择器  div ~ p** 

  # 文本 大小 溢出隐藏

  

  ```
  文本属性
  1. direction  设置文本方向
      值ltr  rtl  
  
  2. letter-spacing 设置字符间距
    可以为负值 
    单位可以使用px
  
  3. text-align:center / left(默认) /right(右边) / justify(文本两边居中)
  
  4. text-decoration 给文本添加修饰
    none  取消文本的默认样式。 
    underline 加上一条下滑线
    overline 上划线
    line-through 穿过文本的一条线 
  
  
  5. text-indent 缩进元素文本的首行
    
  6. text-transform控制元素当中的字母 
    none (默认)/
    capitalize(文本中的每个单词以大写字母开头。) 
    uppercase（定义仅有大写字母） 
    lowercase(小写字母) 
  
  
    ---------------------------------------------------------------------------
  
   1. font-size: 字体大小  
   	14px 
   	14pt 磅
   	14em
   	14rem
  
   	html {
   		font-size:100%;  16px 1rem = 16px
   		font-size:10px;  2rem = 20px;
   	}
  2.font-family : 字体样式 字体族科 
  当前属性通常设置多个字体，包括英文和中文，如果第一个字体不存在，那么就会去找第二个字体，以此类推 。
  	font-family:"Times New Roman","Arial","KaiTi","",""
  
  3.color 字体颜色
  rgb 
  十六进制
  单词
  
  4. font-weight:字体粗细 bold(字体变粗) bolder(更粗) normal(正常) 
  			100-900
  
  5. font-style: italic(斜体字)/oblique(让现有字体发生倾斜)/normal 字体倾斜
  6. text-align: 字体水平对齐方式 left /right /center /justify 能够作用于图片或者文字
  7. vertical-align:top(上) / bottom (下)/middle(中) /baseline(基线)
  8. line-height:行高  
  
  	当行高等于容器的高时，可以实现文本垂直居中。(只适用于单行)
  	当单行文本的行高小于容器高时，可实现单行文本在容器中垂直中齐以上；
  	当单行文本的行高大于容器高时，可实现单行文本在容器中垂直中齐以下（IE6及以下版本存在浏览器兼容问题） 
  9. text-decoration: 文本修饰 none /underline下滑线 / overline上划线 /line-through中横线
  
  10. text-indent:首行缩进  
  	px  em  rem
  11. text-transform控制元素当中的字母 
    none (默认)/
    capitalize(文本中的每个单词以大写字母开头。) 
    uppercase（定义仅有大写字母） 
    lowercase(小写字母) 
  
  12. letter-spacing: 设置字符间距
  
  13. word-spacing:控制英文单词词距
  
  14. layout-flow:horizontal/vertical-ideographic;  控制文本流
  
  	1）horizontal:自左向右
  	2）vertical-ideographic:自上而下
  Tip:专门用于IE的一个属性
  
  --------------------------------------------------------------------------------
  1. 列表属性
  list-style-type:列表样式
  list-style-image:url() 将列表的样式替换成url引入的图片
  list-style-position: outside(外面)/ inside(里面)
  list-style:none;
  
  ---------------------------------------------------------------------------------
  1.border: 边框 宽度 样式 颜色
  border-width
  border-style
  border-color 
  
  ----------------------------------------------------------------------------------
  1. 常用三种图片格式：
  1）jpg :有损压缩格式，靠损失图片本身的质量来减小图片的体积，适用于颜色丰富的图像;(像素点组成的，像素点越多会越清晰 )
  2）gif：无损压缩格式，支持透明，支持动画，适用于颜色数量较少的图像;
  3）png:无损压缩格式，支持透明，不支持动画，(是fireworks的 源文件格式)，适用于颜色数量较少的图像;
  
  -----------------------------------------------------------------------------------
  1.background 背景图像
  background-color 背景颜色
  background-image:背景图片
  background-repeat : 是否平铺
  background-position :背景图像的位置
  background-attachment:背景图像是否固定
  
  ---------------------------------------------------------------------------------
  1. overflow：溢出隐藏
  	visible/hidden(隐藏)/scroll/auto(自动)/inherit;
  
  visible:默认值。当容器内容溢出了容器时，不采取任何行动，任由内容溢出。
  hidden:将溢出的内容隐藏。
  scroll:滚动，如果存在溢出的内容，将以滚动条的形式展示。
  auto:自动。
  
  
  white-space:空余空间 
  normal/nowrap/pre/pre-wrap /pre-line /inherit 该属性用来设置如何处理元素内的空白；
  nowrap ：强制将文本放在一行上显示，如果没有碰到br，就会一直在一行显示。
  pre : 类似于<pre>标签 
  pre-wrap: 保留空白符，但是内容会正常的换行。
  pre-line: 合并空白字符，但是保留换行符。
  
  
  省略号:
  text-overflow:clip不显示省略号/ellipsis显示省略号
  要想让元素能够显示省略号，需要满足下面的条件:
  1. 元素要有具体的宽度
  2. 元素要在一行上显示 white-space:nowrap
  3. 溢出的元素要隐藏掉:overflow:hidden;
  4.才是设置text-overflow:ellipsis; 溢出内容显示为省略号。
   overflow 溢出隐藏  
  	内容溢出 ： 文字 
  	visible 表示默认值，溢出的元素默认让其溢出，不做其处理。
  		Tip: 
  		1.包含子元素的父元素(包含块)在ie6-会出现延伸的情况，变成可以包裹住子元素的宽度。
  		2.在ie7- 会存在另外一种情况，使用button 按钮 或者input type=button 这两种类型的按钮，都会出现
  		按钮当中字越多，按钮两边的padding越大。
  			解决:overflow:visible;
  	hidden 隐藏
  	
  	scroll 滚动 
  		在ie8+ 还有火狐浏览器 在解释overflow:scroll或者overflow:auto的时候会存在padding-bottom的缺失。
  		
  	overflow失效:
  		当子元素处于绝对定位的状态，并且溢出了父元素。这个时候父元素的overflow:hidden或者其他属性都会失效。
  		解决方案:
  			给需要溢出隐藏的包含块设置position:relative;
  			
  	overflow-x:visible/hidden/auto/scroll  overflow-y:visible/hidden/auto/scroll 能够通过这两个属性单独的设置
  		某一个方向的溢出。
  		
  	
  	总结：
  		overflow主要用来解决溢出的问题，溢出可以分两种，一种是文字溢出，一种是元素溢出。
  		
  		
  		
  定位：
  	position: relative;
  	position: absolute;
  	position: fixed;
  	position: static; 默认值
  	
  	position: sticky 粘性定位 ，粘性定位是相对定位和固定定位的结合体。当元素处于屏幕范围之内，元素的定位就相当于是
  	相对定位，而元素一旦脱离了屏幕范围，那么元素的定位属性就会类似于固定定位。
  ```

  # 元素居中的不同情况

  1.元素是一个块级元素并且元素没有脱离标准文档流：

  Margin:0 auto;

  Width:有一个具体的宽度

  2. 已有大小元素在浏览器可视窗口中水平垂直居中。

  ![img](file:///C:\Users\ADMINI~1\AppData\Local\Temp\ksohtml6176\wps1.jpg) 

   

   

  3. 未知大小的元素水平垂直居中

  ![img](file:///C:\Users\ADMINI~1\AppData\Local\Temp\ksohtml6176\wps2.jpg) 

   

  4. 已知大小的元素在父元素中水平垂直居中的方法。

  ![img](file:///C:\Users\ADMINI~1\AppData\Local\Temp\ksohtml6176\wps3.jpg) 

  5. 未知大小的元素在父元素中水平居中的方法

  ![img](file:///C:\Users\ADMINI~1\AppData\Local\Temp\ksohtml6176\wps4.jpg) 

   

   

  6. 未知大小的元素在父元素中水平垂直居中的方法

  ![img](file:///C:\Users\ADMINI~1\AppData\Local\Temp\ksohtml6176\wps5.jpg) 

   

  # 自适应网页效果

  

  1.网页布局中经常要定义元素的宽和高。但很多时候我们希望元素的大小能够根据窗口或子元素自动调整，这就是自适应。自适应的优点：元素自适应在网页布局中非常重要，它能够使网页显示更灵活，可以适应在不同设备、不同窗口和不同分辨率下显示。

  （1）**宽度自适应**   元素宽度设置为100%。（块元素宽度默认为100%）    或者不设置宽度（width）;（宽度是父元素的宽度）（2）**高度自适应**        

  1)自适应元素高度：height:auto;或者不设置;（是子元素撑开父元素的高度） (父元素高度跟随子元素的变化而变化)	   

   2)元素高度自适应窗口高度(子元素的高度跟随父元素的变化而变化) -- 开发app页面使用次数较多         

  ```html
  html,body{height:100%;}
                   
                  <style>
                      html,body{height:100%;}
                      div {background:red;height:100%;}
                  </style>
          
                  <body>
                     <div></div>
                  </body>
  ```

​     		    

  ​     Tip：全屏页面才推荐使用高度100%的方式去开发。               		注：如果设置子元素的高度跟随父元素的高度变化而变化，那么父元素必须有高度

  （3）**元素具备最小高度的自适应**	

  min-height属性：最小高度；(IE6浏览器不识别该属性)	hack1:min-height:value;_height:value;	hack2:min-height:value;  height:auto!important;height:value;          max-width: 最大宽度    max-height: 最大高度   

  （4）**浮动元素父元素高度自适应（高度塌陷）** 

     当子元素有浮动并且父元素没有高度或者加最小高度（min-height:）的情况下父元素会出现高度塌陷   

   hack1：给父元素添加声明overflow:hidden;(触发一个BFC[Block Formatting Context块级格式化上下文],在bfc当中，    浮动元素也会参与计算。)。      

    弊端：会隐藏一些定位在内容区域外侧的元素。                

  hack2:在浮动元素下方添加空div,并给该元素添加            

  声明：div{clear:both; height:0; overflow:hidden;}                  

  这种声明方式在写网页的时候，可以有效的兼容ie6，ie6即是高度没有，也会保留大概6px的高度                 

   只有height:0;和overflow:hidden;搭配使用才可以解决这样的问题。           

   弊端：增加代码的冗余，大量存在一些不必要的元素。    hack3:万能清除浮动法    选择符:after{content:"";clear:both;display:block;height:0;overflow:hidden;visibility:hidden;}            也可以加上 .clearfix{*zoom:1;} 解决ie的问题Tip:    *visibility:hidden/隐藏    *visibility:hidden;和display:none;的区别：    visibility:hidden;属性会使对象不可见，但该对象在网页所占的空间没有改变，等于留出了一块空白区域，而 display:none属性会使这个对象彻底消失不显示，也不再占用位置。

  Tip：    总结：        开发时，通栏宽度依旧保持100%。        测量版心的宽度        元素包含块设置最小高度2. 伪类选择符(伪元素/伪对象)：通常用在块级元素上面    :after 与content属性一起使用，定义在对象后的内容。    :before 与content属性一起使用，定义在对象前的内容。    :first-line  定义对象内第一行的样式。    :first-letter 定义对象内第一个字符的样式。

  # css常用属性浏览器兼容情况

  

  ```
  css常用属性浏览器兼容情况
  
  需求：一个网页能不能够在不同的浏览器里完整的展示！
  1、在网页当中你使用的属性在不同的浏览器里是否可以使用
  
  2、 如果我在开发网页的时候使用的属性不能够在某些浏览器里使用，该怎么解决？
  
  min-height: 不能够在ie6里使用
  
  
  
  -------------------------------------------------------------------
  1. 盒模型属性
  
  	(全兼容)
  	width
  	height
  
  	(IE6-不支持)
  	min-width
  	max-width
  	min-height
  	max-height
  	
  	(全兼容)
  	border
  	border-width
  	border-color
  	border-style
  	
  	(全兼容)
  	margin
  	
  2. 布局类属性
  	注意：IE7-浏览器不支持table类属性值
  	(全兼容)
  	display
  	(全兼容)
  	float
  	clear
  	
  	注意：IE6-不支持固定定位position:fixed
  	(全兼容)
  	position
  	left
  	right
  	top
  	bottom
  	z-index
  	
  	(全兼容)
  	overflow
  	overflow-x
  	overflow-y
  	clip
  	visibility
  
  	(IE不支持)
  	resize
  	
  	
  3. 文本类属性
  	
  	(全兼容)
  	font
  	font-family
  	font-size
  	font-style
  	font-variant
  	font-weight
  	line-height
  	@font-face
  	
  	(全兼容)
  	text-indent
  	
  	(全兼容)
  	text-align
  	vertical-align
  	注意：IE7-浏览器中vertical-align的百分比值不支持小数行高
  	
  	(全兼容)
  	word-spacing
  	letter-spacing
  	
  	(全兼容)
  	text-transform
  	
  	(全兼容)
  	text-decoration
  	
  	(全兼容)
  	white-space
  	
  	(全兼容)
  	text-overflow
  	
  	
  3. 修饰类属性
  
  	(全兼容)
  	background
  	background-color
  	background-image
  	background-repeat
  	background-position
  	
  	(IE8-不支持)
  	background-attachment
  	background-clip
  	background-size
  	
  	(全兼容)
  	color
  
  	(IE8-不支持)
  	opacity
  	
  	(全兼容)
  	命名颜色
  	16进制
  	RGB
  	(IE8不支持)
  	RGBA
  	
  	(全兼容)
  	cursor
  	
  4.其他类属性
  	
  	(全兼容)
  	通配选择器   *
  	元素选择器   div
  	类选择器     .box
  	ID选择器     #box
  	后代选择器   div a
  	分组选择器   h1,p
  
  	(IE6-不支持)
  	属性选择器    h1[class]
  	子元素选择器  ul > li
  	相邻兄弟选择器 div + p
  	(IE7-不支持)
  	通用兄弟选择器 div ~ p
  	
  	伪元素
  	(只有当选择器部分和左大括号之间有空格时，IE6-浏览器才支持)
  	:first-letter
  	:first-line
  
  	(IE7-不支持)
  	:before
  	:after
  	(IE8-不支持)
  	::selection
  	
  	伪类
  	(全兼容)
  	:link
  	:visited
  
  	(IE6-不支持给<a>以外的其他元素设置伪类)
  	:hover
  	:active  
  	
  	单位
  	(全兼容)
  	px
  	in
  	cm
  	mm
  	q
  	pt
  	pc
  	em
  	ex
  	ch
  	
  	(IE8-不支持)
  	rem
  ```

  # 1、颜色和渐变

颜色和渐变：

	颜色：HSL
		通过对色相(H)、饱和度(S)、明度(L)三个颜色通道的变化以及它们相互之间的叠
		加来得到各式各样的颜色。
	
		H：Hue(色调)。0(或360)表示红色，120表示绿色，240表示蓝色，也可取其他数值来指定颜色。
			取值为：0 - 360
		S：Saturation(饱和度)。取值为：0.0% - 100.0%
		L：Lightness(亮度)。取值为：0.0% - 100.0%
	
	HSLA
		此色彩模式与HSL相同，只是在HSL模式上新增了Alpha透明度
		取值：
			H：Hue(色调)。0(或360)表示红色，120表示绿色，240表示蓝色，也可取其他数值
				来指定颜色。取值为：0 - 360
			S：Saturation(饱和度)。取值为：0.0% - 100.0%
			L：Lightness(亮度)。取值为：0.0% - 100.0%
			A：Alpha透明度。取值0~1之间。
	
	opacity：不透明度
	rgba: 不透明度


​	
渐变：
线性渐变和径向渐变

linear-gradient() 线性渐变
	参数：
		to left、to right、to bottom、to top、to left top、to left bottom...
		angle
		color
		
	重复径向渐变
		repeating-linear-gradient()
radial-gradient() 径向渐变



#2、圆角

2.圆角
border-radius:
	可以分别设置四个角也可以使用简写：
		boder-top-left-radius: 左上
		border-top-right-radius:右上
		border-bottom-right-radius:
		border-bottom-left-riadus:
	border-radius：可以设置一个值到四个值。
		顺序：
			1个值：四个角
			2个值: 左上右下 右上左下
			三个值:  左上  右上左下  右下 
			四个值: 左上 右上  右下  左下	

#3、边框图片

3. border-image 边框图片
  目前只有IE11以上才支持。

  border-image 是一个简写值，分别具有以下的属性：
  	border-image-source	图片地址
  	border-image-slice   图片切片
  	border-image-width  图片宽度
  	border-image-outset  图片外凸
  	border-image-repeat  图片重复 

  border-image-slice图像进行切片处理。
  	当进行图像切片后，会将图片切成四个边四个角以及一个中间区域。
  	
  	值：
  		number | 百分比 {1,4}
  border-image-width 图片宽度
  	值：
  		length| number | 百分比{1,4}
  border-image-outset 图像外凸
  border-image-repeat 图像重复

#4、盒子阴影

4. 盒子阴影
  box-shadow:
  h-shadow v-shadow blue spread color inset;

  h-shadow 水平阴影的位置 允许负值
  v-shadow 垂直阴影的位置 允许负值
  blur: 模糊值
  spread:阴影的大小
  color :颜色
  inset :内部阴影

#5、弹性盒子模型部分属性

5. 弹性盒子模型

盒子模型与怪异盒子模型
什么是弹性盒子模型
旧版本弹性盒子模型简单介绍
新版本弹性盒子模型


怪异盒子模型：
	设置的宽度和高度就是元素在网页中实际占据的宽度和高度。
	开启怪异盒子模型：
		**box-sizing:border-box|content-box**
	
弹性盒子模型核心概念：
	主轴
	侧轴
	弹性容器
	弹性子元素
	
弹性容器专用属性：
flex-direction:
	作用：弹性容器中子元素的排列方式(主轴排列方式)【子元素在主轴上的排列方式】
	属性：
		row:默认在一行排列
		row-reverse:反转横向排列（右对齐，从后往前排，最后一项排在最前面。）
		column：纵向排列。
		column-reverse：反转纵向排列，从下往上排，最后一项排在最上面
	
flex-wrap:
	作用:设置弹性盒子的子元素超出父容器时是否换行 
	属性值：
		nowrap: 默认值。规定元素不拆行或不拆列。
		wrap:规定元素在必要的时候拆行或拆列。
		wrap-reverse:规定元素在必要的时候拆行或拆列，但是以相反的顺序。
	
flex-flow: flex-direction和flex-wrap的缩写

align-item:
	作用:设置弹性盒子元素在侧轴（纵轴）方向上的对齐方式
	属性值：
		flex-start：弹性盒子元素的侧轴（纵轴）起始位置的边界紧靠住该行的侧轴起始边界。
        flex-end：弹性盒子元素的侧轴（纵轴）起始位置的边界紧靠住该行的侧轴结束边界。
        center：弹性盒子元素在该行的侧轴（纵轴）上居中放置。（如果该行的尺寸小于弹性盒子元素的尺寸，则会向两个方向溢出相同的长度）。
        baseline：如弹性盒子元素的行内轴与侧轴为同一条，则该值与'flex-start'等效。其它情况下，该值将参与基线对齐。

align-content:
	作用:修改 flex-wrap 属性的行为，类似 align-items, 但不是设置子元素对齐，
			而是设置行对齐(行与行的对其方式)
	属性:
		flex-start没有行间距
		flex-end底对齐没有行间距
		center居中没有行间距
		space-between两端对齐，中间自动分配
		space-around自动分配距离

justify-content:
	作用:设置弹性盒子元素在主轴（横轴）方向上的对齐方式
	属性：
		flex-start默认，顶端对齐
        flex-end末端对齐
        center居中对齐
        space-between两端对齐，中间自动分配
        space-around自动分配距离

# 弹性子元素属性

1.弹性子元素相关属性：
	order：设置弹性盒子的子元素排列顺序。 number排序优先级，数字越大越往后排，默认为0，支持负数。
    flex-grow:设置或检索弹性盒子元素的扩展比率。
    flex-shrink:指定了 flex 元素的收缩规则。flex 元素仅在默认宽度之和大于容器的时候才会发生收缩，其收缩的大小是依据 flex-shrink 的值。
    flex-basis:用于设置或检索弹性盒伸缩基准值。
    flex:设置弹性盒子的子元素如何分配空间。
    align-self:在弹性子元素上使用。覆盖容器的 align-items 属性。

order:设置弹性盒子的子元素排列顺序。 number排序优先级，数字越大越往后排，默认为0，支持负数。

flex-grow:设置或检索弹性盒子元素的扩展比率。
	参数：
	 <integer>：一个数字，规定项目将相对于其他灵活的项目进行扩展的量。默认值是 0。
	瓜分容器的剩余空间。
	什么是剩余空间？
		假设父元素的宽度是500px，
		有三个子元素，每个宽度是100，那么剩余空间就是500 - 100 * 3 = 200。
		而flex-grow就是用来瓜分剩余空间的。
		例如第一个盒子属性为flex-grow:1;那么剩余空间就会被分成一份，第一个盒子额外的占据了这一份。
		如果这个时候第二个盒子flex-grow:2;那么此时剩余空间就被分成三分，第一个盒子占一份，第二个盒子占两份。
		
​		
flex-basis:用于设置或检索弹性盒伸缩基准值。
	参数：<integer>：一个长度单位或者一个百分比，规定元素的初始长度。
	auto：默认值。长度等于元素的长度。如果该项目未指定长度，则长度将根据内容决定。
	
	flex-basis是width的替代品。如果子元素设置了flex-basis或者width，那么在分配空间之前，就会跟父容器预约这么多
	的空间，然后剩下的才归到剩余空间，然后父容器再把剩余空间分配给flex-grow的容器。如果同时设置了flex-basis
	和width，那么width的属性就会被覆盖，也就是说flex-basis的优先级比width高。


​	 
flex-shrink:指定了 flex 元素的收缩规则。
    参数：<integer>：一个数字，规定项目将相对于其他灵活的项目进行收缩的量。默认值是 1。

    当父容器的剩余空间为0的时候，并且默认处于非换行状态的情况下，子元素是没有办法利用弹性容器的剩余空间
    进行扩展的。
    如果如容器的剩余宽度为负数的情况下(子元素的宽度之和大于父容器的宽度)，那么子元素就会被收缩。
    收缩的比例为1:1.
    例如，一个弹性容器中有三个子元素，那么他们的收缩比例就为1:1:1.
    如果这个时候，第一个子元素设置了flex-shrink:2;那么我们就会发现，这个元素比其他两个元素收缩的幅度更大。
    同时呢，因为第一个子元素空间的更多收缩，所以第二个和第三个元素就会获得更多的空间。
    我们假设第二个和第三个盒子收缩比例为x1,那么第一个盒子的收缩比例就为x2.
    
    举个例子：
    
    父元素 500px。三个子元素分别设置为 150px，200px，300px。
    
    三个子元素的 flex-shrink 的值分别为 1，2，3。
    
    首先，计算子元素溢出多少：150 + 200 + 300 - 500 = -150px。
    
    那这 -150px 将由三个元素的分别收缩一定的量来弥补。
    
    具体的计算方式为：每个元素收缩的权重为其 flex-shrink 乘以其宽度。
    
    所以总权重为 1 * 150 + 2 * 200 + 3 * 300 = 1450
        总权重: 收缩比 * 宽度 之和
    三个元素分别收缩：
    溢出值 * 收缩比  * width / 总权重 = 收缩的宽度
    150 * 1(flex-shrink) * 150(width) / 1450 = -15.5
    150 * 2(flex-shrink) * 200(width) / 1450 = -41.4
    150 * 3(flex-shrink) * 300(width) / 1450 = -93.1
    三个元素的最终宽度分别为：
    
    150 - 15.5 = 134.5
    200 - 41.4 = 158.6
    300 - 93.1 = 206.9
    同样，当所有元素的 flex-shrink 之和小于 1 时，计算方式也会有所不同：
    
    此时，并不会收缩所有的空间，而只会收缩 flex-shrink 之和相对于 1 的比例的空间。
    
    还是上面的例子，但是 flex-shrink 分别改为 0.1，0.2，0.3。
    
    于是总权重为 145（正好缩小 10 倍，略去计算公式）。
    
    三个元素收缩总和并不是 150px，而是只会收缩 150px 的 (0.1 + 0.2 + 0.3) / 1 即 60% 的空间：90px。
    
    每个元素收缩的空间为：
    
    90 * 0.1(flex-shrink) * 150(width) / 145 = 9.31
    90 * 0.2(flex-shrink) * 200(width) / 145 = 24.83
    90 * 0.3(flex-shrink) * 300(width) / 145 = 55.86
    三个元素的最终宽度分别为：
    
    150 - 9.31 = 140.69
    200 - 24.83 = 175.17
    300 - 55.86 = 244.14




flex:设置弹性盒子的子元素如何分配空间。
        flex 属性用于设置或检索弹性盒模型对象的子元素如何分配空间。

        flex 属性是 flex-grow、flex-shrink 和 flex-basis 属性的简写属性。
        详情参阅flex缩写文档

align-self:在弹性子元素上使用。覆盖容器的 align-items 属性。值与容器属性一样，只是这个是单独的设置某个元素。

# 响应式布局概念

3. 响应式布局概念
  3.1 相关人物介绍：
  伊桑·马科特（Ethan Marcotte）在2010年首先提出了响应式网页设计（RWD,Responsive Web Design）这个术语。
  在他的一篇文章《Responsive Web Design · An A List Apart Article》中他将已有的三种发开技巧（弹性
  图片，弹性网格布局，媒体与媒体查询） 进行了整合，命名为响应式网页设计。
  那什么才是真正的响应式设计？马科特说，真正的响应式设计方法不仅仅是根据可视区域大小而改变网页布局，而是要
  从整体上颠覆当前网页的设计方法，是针对任意设备的网页内容进行完美布局的一种显示机制。

3.2 响应式网页浏览
    了解响应式网页的特性

3.3 当今流行的网页布局方案
固定布局：以像素作为页面的基本单位，不管设备屏幕及浏览器宽度，只设计一套尺寸；

可切换的固定布局：同样以像素作为页面单位，参考主流设备尺寸，设计几套不同宽度的布局。通过识别的屏幕尺寸或
    浏览器宽度，选择最合适的那套宽度布局；

响应式布局：对页面进行响应式的设计实现，需要对相同内容进行不同宽度的布局设计，有两种方式：pc优先（从pc
端开始向下设计）；移动优先（从移动端向上设计）；无论基于那种模式的设计，要兼容所有设备，布局响应时不
可避免地需要对模块布局做一些变化（发生布局改变的临界点称之为断点）。

弹性布局：以百分比作为页面的基本单位，可以适应一定范围内所有尺寸的设备屏幕及浏览器宽度，并能完美利用有效空
    间展现最佳效果；

混合布局：同弹性布局类似，可以适应一定范围内所有尺寸的设备屏幕及浏览器宽度，并能完美利用有效空间展现最佳效果；
    只是混合像素、和百分比两种单位作为页面单位。

3.4 响应式布局的优缺点
设计特点：
    面对不同分辨率设备灵活性强
    能够快捷解决多设备显示适应问题
缺点：
    兼容各种设备工作量大，效率低下
    代码累赘，会出现隐藏无用的元素，加载时间加长
    其实这是一种折中性质的设计解决方案，多方面因素影响而达不到最佳效果
    一定程度上改变了网站原有的布局结构，会出现用户混淆的情况

3.5 开发响应式网页的前期准备

3.5.1 Meta标签的设置
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0,minimum-scale=1.0,  user-scalable=no">
    这段代码的几个参数解释：
    width = device-width：宽度等于当前设备的宽度
    initial-scale： 初始的缩放比例（默认设置为1.0）
    minimum-scale：允许用户缩放到的最小比例（默认设置为1.0）
    maximum-scale：允许用户缩放到的最大比例（默认设置为1.0）
    user-scalable：用户是否可以手动缩放（默认设置为no，因为我们不希望用户放大缩小页面）


3.5.2 meta标签其他可选设置

H5页面窗口自动调整到设备宽度，并禁止用户缩放页面
<meta name="viewport" content="width=device-width,initial-scale=1.0,minimum-scale=1.0,maximum-scale=1.0,user-scalable=no" />
忽略将页面中的数字识别为电话号码
<meta name="format-detection" content="telephone=no" />
忽略Android平台中对邮箱地址的识别
<meta name="format-detection" content="email=no" />
当网站添加到主屏幕快速启动方式，可隐藏地址栏，仅针对ios的safari
<meta name="apple-mobile-web-app-capable" content="yes" />
<!-- ios7.0版本以后，safari上已看不到效果 -->
将网站添加到主屏幕快速启动方式，仅针对ios的safari顶端状态条的样式
<meta name="apple-mobile-web-app-status-bar-style" content="black" />

3.5.3 rem 和 vw/vh
rem是以html根元素的字体大小为参考。
默认情况下，1rem = 16px，此时html相当于font-size:100%。

html {
    font-size:100px;
   }

 1rem = ;


vh|vw这两个单位，以视口为参考。
视口单位中的“视口”，桌面端指的是浏览器的可视区域；移动端指的就是Viewport中的Layout Viewport。

    1vw等于视口宽度的1%。
    1vh等于视口高度的1%。
    Tip：并且会随着视口的变化而变化。

3.5.4 什么是断点？
断点，响应式网页发生变化的临界点。

```
 常用断点值

    320px
    480px
    768px
    1024px
```

# 3.5.5 什么是媒体查询，响应式网页与媒体查询的关系

媒体查询是css当中的一种技术，通过这种技术可以判断用户的浏览器宽度，类型，以及横屏还是竖屏等。

响应式网页的实现方式有很多，主流方式是通过媒体查询的形式来实现响应式网页。

3.5.6 媒体查询特性
媒体查询可以让我们根据设备显示器的特性（如视口宽度、屏幕比例、设备方向：横向或纵向）为其设定CSS样式，
媒体查询由媒体类型和一个或多个检测媒体特性的条件表达式组成。媒体查询中可用于检测的媒体特性有 width 、
height 和 color （等）。使用媒体查询，可以在不改变页面内容的情况下，为特定的一些输出设备定制显示效果。

# 3.5.7 媒体查询基本语法

@media 媒体类型  关键字 (条件1) 关键字 (条件2) ... {
    css code
}

常用媒体类型：
    all     所有设备
    aural    听觉设备
    braille   点字触碰设备
    print    打印
    tty      打字机设备
    tv      电视机等设备
    screen  显示器、笔记本、电脑等设备
    ...

    上述的设备有很多，只是简单的陈述几种，但是我们常用的设备只有all和screen

关键字：
    and 并且 和
    not 否定、排除
    only 限定
    or 或者
条件：
    min-width:400px

媒体查询语法示例:
    @media all (min-width:480px) {
        html {
            background:red;
        }
    }

    上述示例表示当用户设备屏幕处于最小宽度为480px以上的时候，网页的背景颜色为红色
    
    /* 竖屏 */
    @media screen and (orientation:portrait) {对应样式}
    
    /* 横屏 */
    @media screen and (orientation:landscape){对应样式}

3.5.8 常用断点值

    320px
    480px
    768px
    1024px

3.5.9 css2中媒体查询的用法

其实并不是只有CSS3才支持Media的用法，早在CSS2开始就已经支持Media，具体用法，就是在HTML页面的head标签中插入如下的一段代码
<link rel="stylesheet" type="text/css" media="screen" href="style.css">;
想知道现在的移动设备是不是纵向放置的显示屏，可以这样写：
<link rel=“stylesheet” type=“text/css” media=“screen and  (orientation:portrait)”  	href="style.css">
orientation:portrait：指定输出设备中的页面可见区域高度大于或等于宽度
landscape：除portrait值情况外，都是landscape
第一段的代码也用CSS2来实现，让它一样可以让页面宽度小于960的执行指定的样式文件：
<link rel="stylesheet" type="text/css" media="screen and (max-width:960px)" href="style.css">

# 3.5.10 移动端优先和pc端优先



在开发响应式网页的时候，我们有两种选择，一种是从移动端开始开发然后逐渐升级到pc，这种方式叫做移动端优先
pc端优先则正好相反。

# flex缩写

```
简介：
flex是flex-grow,flex-shrink和flex-basis的缩写，flex属性值可以只指定一个属性的值，而另外的属性值采
用各自在flex属性中的的初始值，但是有一点要注意的是：flex属性中flex-grow和flex-basis的初始值和它们原始
的默认值不同，至于为什么不同，mdn中有明确的说过这样的设计是为了让「flex」缩写在最常见的情景下比较好用。



flex中对应各属性的初始值：

flex-grow
  flex-grow用于设置各item项按对应比例划分剩余空间，若flex中没有指定flex-grow,则相当于设置了
    flex-grow:1

flex-shrink
  flex-shrink用于设置item的总和超出容器空间时，各item的收缩比例，若flex中没有指定flex-shrink,
    则等同于设置了flex-shrink:1


flex-basis
  flex-basis用于设置各item项的伸缩基准值，可以取值为长度或百分比，如果flex中省略了该属性，则相当
    于设置了flex-basis:0.

flex的不同取值
  flex的值的完整写法是[<flex-grow> <flex-shrink> <flex-basis>],不过它的取值还有可能是单个数字
    或者单个百分比等，不同种类的取值所表示的意思是大有不同的。

flex值为none
  当flex为none时,等同于flex: 0 0 auto;

flex值为auto
  当flex为auto时，等同于flex: 1 1 auto;

flex值为一个非负数字
  当flex取值为一个数字，则该数字是设置的flex-grow值，其它两个属性用初始值，如flex:1时，
    等同于flex: 1 1 0%

flex值为两个非负数字
  当flex取值为2个数字时，相当于设置的flex-grow和flex-shrink值，flex-basis取值为初始值，
    如flex:1 0时，等同于flex: 1 0 0%

flex值为一个数字和一个长度或百分比时
  当flex取值为1个数字和1个长度或百分比时，设置的是flex-grow和flex-basis的值，flex-shrink值
    时初始值，如flex:1 20%,等同于flex: 1 1 20%
```

 # 1.主流浏览器  

 ```css
谷歌    -webkit-         

火狐   -gecko-  

safari   -webkit- 

opera     -blink-  -presto-

ie     -trident-

 ```





2.浏览器前缀

使用一些css3的属性的时候应该考虑到不同浏览器的内核兼容情况，需要针对不同的内核使用不同的浏览器前缀。

```css
webkit内核:   -webkit-

firefox Gecko内核:  -moz-

opera :   -o-

trident内核  :  -ms-

-webkit-border-radius:10px;

-moz-border-radius:10px;

-ms-border-radius:10px;

-o-border-radius:10px;

border-radius:10px;

浏览器前缀自动补全的网址:http://autoprefixer.github.io
```







3. 选择器选择器

   # 属性选择器

   

4. Tip：E ---> elements 元素  attr属性   value 值

   ```css
   E[attr]
   E[attr=value]
   E[attr^=value]
   E[attr$=value]
   E[attr*=value]
   E[attr~=value]
   E[attr|=value]
   http://static.wenku.bdimg.com/static/wkcommon/pkg/pkg_wkcommon_base_z_a372731.png
   ```

   

   # 3.2 结构伪类选择器 

   

   ```css
   E:nth-of-type()   / E:nth-child()
   E:first-of-type  / E:first-child
   E:last-of-type  / E:last-child
   E:only-of-type / E:only-child 
   
   
   :nth-child(x) 选择第x个元素
   :nth-child(n) 全选
   :nth-child(2n) 选择偶数
   :nth-child(2n+1) 奇数
   
   :first-child 第一个
   :last-child 最后一个
   
   :only-child 唯一的一个子元素
   
   :nth-child(x) 选择的是指定位置的子元素
   :nth-of-type(x) 选择的是指定位置的元素
   Tip:  当我们使用:nth-of-type的时候，前面一定要加上元素名不然太猛了
   
   E:first-of-type 同级的情况下，选择第一个元素
   E:last-of-type 同级的情况下选择最后一个元素
   E:only-of-type 同级的情况下选择唯一的元素
   
   :root  根元素 等同于 html
   :not 
   :empty
   :target
   ```

   **:root 大概等价与html，但是还有一定区别:**

   1. 优先级不同
     root的优先级高于html
     2.范围不同
     html 只适用于html，root在其他的一些语言里也可以用到。

   :not 取相反的操作
   例如: ul li:not(.a) 选择的是类名不是a的li元素

   :empty  选取为空的元素
   :target  选取目标元素

   # 3.3 状态伪类选择器

   ```css
   :focus 
   :checked
   ::selection
   :first-letter    选取第一个字符
   :first-line      选取第一行
   
   
   :focus  元素获得焦点
   :checked  元素被选中
   
   ::selection 表示被光标选取中
   
   
   
   :enabled
   :disabled 
   :read-write
   :read-only 
   :before
   :after  
   
   
   :enabled 选择的是可用状态的标签
   :disabled 选择的是禁用状态的标签
   :read-write 可读可写 正常状态的input就可以被选中
   :read-only 可读，只有在input的状态为readonly时才会被选中
   
   ----
   input状态:
   disabled 禁用
   required 必填
   readonly 只读
   ----
   ::before ,::after 
   :after , :before
   
   ```

   

   ```
   你会在别人的代码中看到上面的现象，::after这样的写法，那么经过测试发现，我们:after和
   ::after都可以有效果。
   那么他们的区别在哪里？
   
   首先，:after表示伪类，诞生于css2.1，而到了css3的时候就将:after这样的伪类升级为两个冒号。
   二者都有效果。
   
   但是:after 和 ::after 有什么区别?
   css3中定义，一个冒号表示伪类，两个冒号表示伪元素。
   
   伪类和伪元素有什么区别?
   伪类:当标签进行css样式操作的时候，使用伪类选择操作的样式相当于作用到了元素的“本身”。
   伪元素:当标签进行样式操作的时候，相当于将样式作用到了一个"虚拟的标签"的身上。
   ```

   # 文本 TEXT

   ```css
   text-shadow   文字阴影
   text-stroke    文字描边
   text-overflow   文字溢出隐藏
   direction    文字排列方式
   word-break 规定自动换行的处理方式
   word-wrap  允许长单词或 URL 地址换行到下一行
   @font-face   嵌入字体 
   
   
   
   text-shadow:
   	参数:
   		x x轴的偏移量
   		y y轴的偏移量
   		blur 模糊值  带有单位  值越大越模糊，负值消失
   		color 颜色
   		多阴影
   		
   
   text-stroke ： 文字描边
   	参数:
   		w 描边的宽度
   		color 颜色
   		
   	Tip:谷歌浏览器需要使用浏览器前缀  
   		目前只有谷歌支持(待测试)
   
   
   word-break 自动换行的处理方式
   	参数：
   		normal 
   		break-all 允许在单词内换行
   		keep-all 只允许在空格或者连字符处换行
   		
   
   word-wrap  
   	参数：
   		normal 
   		break-word  在长单词或url地址内部进行换行
   
   
   字体图标：
   引入字体图标首先
   	需要下载字体图标库
   	下载完成之后引入对应的css文件
   	在给需要的标签设置字体图标对应的类名
   全套字体图标：
   	http://www.bootcss.com/p/font-awesome/
   定制字体图标：
   	https://icomoon.io/app/#/select
   	
   总结：
   	为什么使用雪碧图/css精灵图
   	减少客户端向服务端发送的http请求的次数，减少服务端的压力
   	
   	为什么使用字体图标
   		能够自由的按照文字的方式对图标进行适当的更改。
   ```

   

   # backgound   背景

   ```css
   background-size
   background-origin
   background-clip
   多背景设置
   
   
   
   background-size:
   	参数：
   		length   带有单位的数值
   		percentage   百分比
   		cover   覆盖整个盒子 等比放大
   		contain  把整个图片完整的包裹进盒子当中 等比放大
   		
   	background-size：100px;
   	当这个属性设置一个值的时候，这个值表示宽度，高度为自适应。
   		Tip：当设置一个值的时候，不要错误的把高度也想象成这个值。
   	如果设置两个值的时候，第一个值表示宽度，第二个值表示高度。
   	
   	当值设置为百分比的时候，是以父容器的宽度和高度为参考。
   	cover 表示不去考虑图片能不能够完整的显示，而是要把容器占满。
   	contain 表示不去考虑图片是否占满盒子，而是考虑图片显示完整。
   	
   	300 400
   	宽高比3:4
   
   		Tip:ie6-8不能够支持
   		
   	插件:backgroundsize.min.htc
   	
   background-origin  背景位置
   	相关属性:
   		padding-box   图片会占满padding+内容
   		border-box    图片会占满border+padding+内容
   		content-box  图片会占满内容区域
   		
   
   		
   background-clip 背景裁切 
   
   	相关属性:
   		padding-box
   		border-box   默认值
   		content-box
   	
   	
   多背景：
   	/*多背景，顺序靠前，层级就高*/
   	background: url(./images/xx1.jpg) no-repeat left top,
   				url(./images/xx3.jpg) no-repeat left bottom,
   				url(./images/xx4.jpg) no-repeat right top,
   				url(./images/xx5.jpg) no-repeat right bottom,
   				url(./images/xx2.gif) no-repeat center center;
   		
   ```

   

   

   

