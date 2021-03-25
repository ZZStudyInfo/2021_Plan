# h5
1. `<!DOCTYPE html>`：是一种标准通用标记语言的文档类型声明。 告诉解析器用什么文档类型定义（DTD）来解析文档，出错则向后兼容，即新版本兼容老版本

2. xhtml和html的区别：   
  - XHTML 1.0是基于HTML 4.01的，没有引入任何新标签或属性，语法上更加严格。几乎所有的网页浏览器在正确解析HTML的同时，可兼容XHTML
  - HTML是一种基于标准通用标记语言（SGML）的应用，而XHTML则基于可扩展标记语言（XML），其实是平行发展的两个标准。建立XHTML的目的就是实现HTML向XML的过渡。
  - 写法要求不同：xhtml必须结束标记，对大小写敏感，标签名必须用小写字母，必须合理嵌套，XHTML 文档必须拥有根元素，属性必须用“”括起来，属性必须赋值等，html反之。

3. W3C——万维网联盟。W3C 最重要的工作是发展 Web 规范

4. 对WEB标准的理解与认识：
标签闭合、标签小写、不乱嵌套、提高搜索机器人搜索几率、使用外 链css和js脚本、结构行为表现的分离、文件下载与页面速度更快、内容能被更多的用户所访问、内容能被更广泛的设备所访问、更少的代码和组件，容易维 护、改版方便，不需要变动页面内容、提供打印版本而不需要复制内容、提高网站易用性.

5. 常用浏览器机器内核
  - Trident内核（IE内核）：IE

  - webkit内核：chrome、Safari

  - Gecko内核（火狐内核）：Mozilla firefox（火狐浏览器）

  - Presto内核：Opera

6. 元素类型
  - 块元素：div ul ol li dl  h1 h2 h3 ....p

    特点：独占一行，其宽度自动填满父元素宽度，可以设置width、height、padding、margin。
  - 行内元素：a span i

    特点：相邻的行内元素会排列在同一行内，其宽度随元素的内容而变化，不可设width和height；margin和padding水平方向有效，竖直方向无效。
  - 行内块元素： img  input meta area  command embed  source  br hr link

    特点：带有宽高并且能设置宽高，带有功能性 
    
7. 盒模型（由content、padding、border、margin组成）
  - w3c盒模型： content = content； 占据位置为content + padding + border + margin
  - ie盒模型即怪异盒模型： content= content + paading + border；  占据位置为content + margin

    拓展：box-sizing: content-box（标准盒模型default）/border-box（怪异盒模型）/inherit（从父元素继承 box-sizing 属性值）

8. h5新特性（语义化的HTML）
  - 语义化内容标签（header/nav/footer/aside/article/section/tbody/tfooter/selct/button/textarea..）  
    优点：内容结构化，代码语义化，便于维护阅读理解，便于浏览器、搜索引擎解析，有利于seo。
  - 表单控件： calendar、date、time、email、url、search
  - webworker/websocket/geolocation/audio/video等新技术
  - Canvas+WEBGL等技术，实现无插件的动画以及图像、图形处理能力；
  - 本地存储，可实现offline应用；?     
  - websocket，一改http的纯pull模型，实现数据推送的梦想；?     
  - MathML，SVG等，支持更加丰富的render；

    >拓展：HTML5已经远远超越了标记语言的范畴，其背后是一组技术集。HTML5的好处还在于对跨浏览器方面的推动，因为4时代，由于语言本身的弱，导致了浏览器各自为政扩展开发了很多特性，导致浏览器之间不兼容，跨浏览器的应用开发是一件十分令人头疼的事情。


9. ifram标签缺点： 
	- 阻塞主页面的onload事件；	
	- 搜索引擎的检索程序无法解读这种页面，不利于seo;
	- iframe和主页面共享连接池，而浏览器对相同域的链接有限制，所以会影响页面的并行加载
	解决方法：通过js动态给iframe添加src属性值


# css
1. css3新特性
  - font-face(定义自己的字体)、box-shadow:10px 10px 5px #888（盒阴影）、text-shadow:5px 5px 5px #FF0（水平阴影，垂直阴影，模糊距离，阴影颜色）、word-wrap：break-word、border-image: url(border.png) 30 30 round、text-overflow、transform、gradient、border-image、animation、rgba、fiter滤镜等
  - 弹性布局flex（试用场景：弹性布局适合于移动前端开发，在Android和ios上也完美支持）/栅格布局grid/多列布局
  - 媒体查询：定义两套css，当浏览器的尺寸变化时会采用不同的属性
  - 增加了更多选择器
    伪类/状态选择： nth-child()/nth-of-type()/:hover/visited/: chcked/:disabled  

2. css3选择器以及优先级
  - 选择器： id选择器、class选择器、元素选择器（div/ul/li）、全局选择器（*）、组合（div#wrap）/后代（div p）/群组（div, p）选择器、属性选择器、子元素选择器（div>p）、相邻兄弟选择器（div+p）、伪类选择器（::after）、状态选择器（:checked,:disabled）等。附：[css选择器手册]（https://www.w3school.com.cn/cssref/css_selectors.asp）  

    >注意：类名的第一个字符不能使用数字！它无法在 Mozilla 或 Firefox 中起作用。
  - 优先级：!important > 行内样式 > ID选择器 > 类选择器 > 标签 > 通配符 > 继承 > 浏览器默认属性（同一级别：后写的会覆盖先写的）
    > 注意： css选择器的解析原则：选择器定位DOM元素是从右往左的方向，这样可以尽早的过滤掉一些不必要的样式规则和元素
      
3. css引入方式以及link和@import区别 style标签写在body后与body前区别
  - 引入方式：  
    1.外部样式表 `<head><link rel="stylesheet" type="text/css" src="style.css"></head>`  
    2.内部样式表 `<head><style type="text/css">此处为样式 </style></head>`  
    3.内联样式 `<p style="color:red;font-size:16px;">内联样式</p>`  
    4.导入样式 `<head><style type="text/css"> @import url("style.css") </style></head>`   

  - link和@import区别（推荐使用link）：   
    1.link除了引用样式文件，还可以引用图片等资源文件，而import只引用样式文件   
    2.link引用CSS时，在页面载入时同时加载；@import需要页面网页完全载入以后加载。  
    3.link是XHTML标签，无兼容问题；@import是在CSS2.1提出的，低版本的浏览器不支持。  
    4.link支持使用Javascript控制DOM去改变样式；而@import不支持。    
    
  - style标签写在body前和写在body后的区别：  
    1.写在body标签前利于浏览器逐步渲染： resources downloading->CSSOM+DOM->RenderTree(composite)->Layout->paint  
    2.写在body标签后由于浏览器以逐行方式对HTML文档进行解析，当解析到写在尾部的样式表（外联或写在style标签）会导致浏览器停止之前的渲染，等待加载且解析样式表完成之后重新渲染，在windows的IE下可能会出现FOUC现象（即样式失效导致的页面闪烁问题）、重绘或重新布局。  
    >html标准中允许body中出现link，而不允许style  

4. 优雅降级和渐进增强
  - 渐进增强：低版本浏览器（基本功能）—>高版本浏览器（兼容高版本追加功能）
  ```
   .transition { /*渐进增强写法*/  适用低版本用户居多的终端
      -webkit-transition: all .5s;  //webkit —>safari/ 谷歌（Blink）
      -moz-transition: all .5s;     //gecko —> firefox
      -ms-transition: all .5s;	    //trident —>  ie 4以上
      -o-transition: all .5s;       //presto —> opera
      transition: all .5s;
	  }
  ```
  - 优雅降级：高版本浏览器（完整功能）—>低版本浏览器（兼容使其正常浏览）
  ```
    .transition { /*优雅降级写法*/ 使用高版本用户居多的终端
      transition: all .5s;
      -o-transition: all .5s;
      -ms-transition: all .5s;
      -moz-transition: all .5s;
      -webkit-transition: all .5s;
		}
  ```

5. 常见的兼容问题  
  - 不同浏览器的标签默认的margin和padding不一样：*{margin:0;padding:0;}  
  - 双倍边距： 块元素 + 浮动 + margin + 贴边：块元素{display: inline}   
  - ie6不识别较小高度，默认16，解决：{font-size : 0 } 、{overflow: hidden}、line-height 小于你设置的高度 
    > 拓展：  
      1.单行文本垂直居中：把line-height值设置为height一样大小的值；  
      2.多行文本垂直居中：需要设置display属性为inline-block。  
  - Chrome 中文界面下默认会将小于 12px 的文本强制按照 12px 显示，解决：{font-size:20px;-webkit-transform:scale(0.5);}  
  - 鼠标指针bug: cursor:hand（只有ie识别）-> cursor:pointer  
  - 表单元素行高不一致 vertical:middle /float: left  
  - 最小高度不兼容ie6： min-height:100px;_height:100px  

6. margin常见问题
 - 若父盒子没有paading-top,border-top，第一个子元素的margin-top会作用在父元素上，即无限传递。
    >解决办法:  
        1.父元素：overflow:hidden/float: left/padding: 1px/border: 1px solid  transparent/zoom: 1;  
        2.子元素：float:left/display:inline;
  - 重合选大的问题：父子，兄弟元素重叠。
    >解决办法:  
        给其中一个元素外面包裹一个父元素，父元素加上overflower: hidden（检索子元素高度）,   
        两个元素便不属于同一个BFC，就不会发生margin重叠了


7. padding和margin适用场景
  - 何时使用margin：
    需要在border外侧添加空白
    空白处不需要背景色
    上下相连的两个盒子之间的空白，需要相互抵消时。
  - 何时使用padding：
    需要在border内侧添加空白
    空白处需要背景颜色
    上下相连的两个盒子的空白，希望为两者之和。

8. BfC


9. 清除浮动


10. 居中


11. 弹性盒子


12. 常见布局


13. 移动端响应式布局（px, em, rem, vw）
14. sass less
15. 浏览器是怎样解析CSS选择器的以及css优化提高性能
15. css问题：
  - 图片精灵
  - 品字和三角形实现
  - ::before 和 :after中双冒号和单冒号有什么区别
  - 怎么让Chrome支持小于12px 的文字
  - 绘制1px,0.5px高的线，
  - 可继承css
  - display:none；visibility:hidden


  
   