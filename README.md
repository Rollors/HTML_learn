# HTML_learn
HTML语言描述页面结构  
CSS 美化页面  
Javascript 从交互角度，提升用户体验  
搜索引擎对网页的抓取通过关键字
*** 

**_HTML(超文本标记语言)_**：超文本是用过超链接的形式将文本组合在一起，标记是对网页中每部分的功能进行标记  
*   标签：元素  
    *   由尖括号包围、成对出现   --`<title>百度一下</title>`成为元素  
    *   单独出现               --`<img />`  
    *   标签之间有嵌套关系、缩进 --外层外父元素，内层为子元素，还有兄弟元素，标签的嵌套形成DOM树(JS操作DOM树)即文档对象树  
*   标签：属性
    *   一个标签有多个属性，属性没有书写顺序 --`<img src="" alt=""/>`
*   文件结构
    *   .htm 或 .html文件
        *   `<!DOCTYPE html><html lang="en"><head><meta charset="UTF-8"><title>前端开发课程首页</title></head><body>
    课程内容包括HTML、CSS、JS</body></html>` --其中`<!DOCTYPE html>`表示当前文档符合HTML5，lang属性提供给搜索引擎信息、表示网页以中文或者英文显示，meta代表元数据
    *   字符集与编码`(源文件保存编码方式与声明编码方式不一致会出现乱码)`
        *   字符：文字与符号
        *   字符集：语言文字，比如英文字符集、汉字字符集
        *   编码：将字符与二进制码对应
*   HTML基本标签
    *   标题`(h1~h6)`
        *   一个页面建议只有一个h1  每一级标题可以使用CSS样式且默认样式不一样
    *   段内换行`(br)`
        *   单独出现的标签，直至结束`<p>这是一个段落。<br/>注意规范的写法保留</p>`
    *   段内分组`(span)`
        *   组合行内元素，以便通过CSS样式来格式化
    *   段落`(p)`
        *   对p标签里面的内容自动分段、忽略连续空格（只显示一个空格）、不会显示空行和人为换行
        *   连续空格
    *   预留格式`(pre)`
        *   定义预格式化的文本，文本中的空格和换行符会被保留
    *   水平线`(hr)`
        *   `<p>最新中国人口普查报告</p><hr /><p>指出</p>`
    *   注释
        *   ` <!---->`
    *   超链接标签`a`
        *   单击超链接可跳转页面`<a href="www.baidu.com">百度</a>、<a href="news.html">新闻</a>跳转本站点其他网页、虚拟超链接href="#""`
    *   图像标签`img`
        *   图像格式
            *   jpg --有损压缩、色彩丰富图片
            *   gif --简单动画、背景透明
            *   png --无损压缩、透明、交错、动画
        *   插入图像
            *   src --图片来源
            *   alt --当图片没有找到时，这就是图片的替换文本：路径+文件名
        *   绝对路径与相对路径
            *   绝对路径 --以根目录为基准：src为C:/site/mm.jpg
            *   相对路径 --以该文档所在位置为基准：如HMTL文件下的test.html插入图片：src为mm.jpg
            *   当图片路径为site/mm.jpg与.html文件的路径为site/c/j.html，则src为../mm.jpg
            *   当图片路径为site/image/mm.jpg与.html文件的路径为site/c/j.html，则src为../image/mm.jpg
    *   div`会独占一行`
        *   区域div --页面划分为各个区域，成对使用，属性align,结合CSS样式分别定义样式,id属性唯一
    *   ul、ol、li
        *   无序列表，ul
        *   有序列表，ol
    *   table、tr、td
        *   表格 --border表格线的粗细，th为表头单元格
    *   表单`form`
        *   表单 --一个区域、采集用户信息`<form action="数据处理网页">表单元素</form>`    action属性表示收集来的数据交由那个页面来处理（后端页面）
        *   表单元素 --文本框、按钮、单选、复选、下拉、文本域
            *   `<input type="text/password" name="" />` --text表示文本框、password表示密码框；文本框明文显示、密码框则是*号显示;当表单元素需要提交给后端页面处理时，后端根据name属性知道数据来自哪个表单元素;
            *   按钮 `<input type="submit" value="提交" />` --submit表示提交
            *   重置 `<input type="reset" value="重置" />`
            *   单选框、复选框 `<input type="radio/checkbox" value="值" name="名称" checked="checked" />` --radio单选、CheckBox复选、value表示提交到后端的数据、name表示当前这一项的名称、checked表示是否默认被选择；单选时，name要一致
            *   下拉 `    <select><option selected="selected"></option></select>` --为节省页面空间;selected="selected"表示被选中的；
            *   文本域 `<textarea name="" id="" cols="30" rows="10"></textarea>` --rows表示行；cols表示列数；
***
#CSS样式 --父层的样式被子层继承
*   CSS概述
    *   层叠样式表(CSS):随着技术的发展，将网页的内容与样式相分离，便于修改，相同的内容可以给予不同的样式；
*   CSS语法
    *   `p{ 
    font-size:12px;
    color:blue;
    font-weight:bold;
}` --p为选择器、花括号里面：左边是属性名，右边是属性值；最后一条声明可以没有分号。
*   CSS添加方法
    *   行内 --`<p style="color:``red;">天使投资指早期投资，尤其指个人早期投资。</p>`
    *   内嵌 --添加到`<head>p{font-size:12px; /*字号*/color:blue;     /* 颜色*/font-weight:bold;/*粗细*/}</style></head>` 内嵌只对单个页面有效，需要重新定义。
    *   链接样式 --`<head><link rel="stylesheet" href="css/style.css/><head/>` 内容与样式完全分离，维护方便，如果需要修改网页风格只需要修改样式文件
    *   优先级 --行内样式>内嵌>链接样式
*   CSS选择器
    *   标签选择器 --使用HTML标签
    *   类别选择器 --标签内部的class属性如`.class` 类别可以引用多次
    *   ID选择器 --标签内部的ID属性如`#ID` ID只能被引用一次
    *   嵌套声明 --标签之间的嵌套如`p span{}`空格分隔
    *   集体声明 --多个标签一起声明如`p,span{}`逗号分隔
    *   全局声明 --如`*{}`
*   CSS样式
    *   文本
        *   单位与颜色
            *   px --像素
            *   em --字符`1em表示1个字符` 自动适应用户所使用的的字体
            *   % --百分比 由继承来的样式来决定，占百分之多少
            *   颜色 --RGB取值如`rgb(x,x,x)` or 十六进制数如`#ff0000` or `rgba(x,x,x,a)` or `red blue green` or `rgb(x%,x%,x%)`
        *   text
            *   color --文本颜色
            *   letter-spacing --字符间距
            *   line-height --行高
            *   text-align --对齐
            *   text-decoration --装饰线
            *   text-indent --首行缩进
        *   font
            *   font --在一个声明中设置左右的字体属性
            *   font-family --字体系列
            *   font-size --字号
            *   font-style --字体风格
            *   font-weight --粗体
    *   背景
        *   background 
        *   background-color --背景颜色
        *   background-image --背景图片`url("log.jpg")` 会覆盖背景颜色
        *   background-repeat --背景图片重复填充方式 棋盘格填充，在水平和垂直两个方向填充；横向填充`repeat-x` 纵向填充`repeat-y` 背景图片只出现一次`no-repeat`
    *   超链接四种状态`:伪类选择器`
        *   a:link --普通的、未被访问的链接
        *   a:visited --用户已访问的链接
        *   a:hover --鼠标指针位于链接上方悬停
        *   a:active --链接被点击的时刻 激活
        *   四种状态设置顺序 --`a:link,a:visited>a:hover>a:active`
    *   列表样式`无序列表ul 有序列表ol 共用样式`
        *   list-style --所有用于列表的属性设置在一个声明中
        *   list-style-imae --为列表项标志设置图像
        *   list-style-position --标志的位置
        *   list-style-type --标志的类型 
    *   表格样式`奇偶选择器 tr:nth-child(odd|even) nth-child表示第n个子元素 括号里表奇偶行`
        *   表格大小`width height`
        *   表格边框`border border-collapse`
*   CSS页面布局与定位
    *   外层 --container
    *   上层 --header
    *   导航条 --main`navbar menu content sidebar`
    *   下层 --footer
    *   盒子模型`页面上的区域、图片、导航、列表、段落度可以看做是一个盒子`
        *   盒子模型组成
            *   content --内容
            *   height --高度
            *   width --宽度
            *   border --边框 具有四个方向
            *   padding --内边距 内容到边框之间的距离 具有四个方向
            *   margin --外边距 border之外的间距 具有四个方向
            *   text-align --图片文字居中
            *   除了内容，全是属性的名字即CSS样式 
        *   内容溢出`overflow`
            *   hidden --超出部分不可见
            *   scroll --显示滚动条
            *   auto --如果有超出部分，显示滚动条
        *   border
            *   border-width --边框宽度`px thin medium thick`
            *   border-style --边框风格 虚线、实线`dashed dotted solid double`
            *   border-color --颜色`red `
            *   border --`width style color`
        *   padding和margin`对浏览器默认设置清零`
            *   top --如`padding-top margin-top`
            *   left
            *   right
            *   bottom
            *   `margin:1px 1px 1px 1px`对应以上四个方向上、右、下、左;上下相对、左右相对
            *   margin的合并 --垂直方向合并，水平方向不合并；选择两个盒子外边距大的作为两个盒子的间距；
            *   margin设置div居中`margin:0 auto`浏览器自动计算，因为水平方向为auto
    *   定位机制
        *   概述 --找到盒子模型在页面中的位置
        *   文档流 --从上到下，从左到右依次排列，默认方式
            *   元素分类 --`block inline inline-block` 
                *   block属性独占一行，元素高、宽、外边距以及内边距度可以设置 --如`div p h1 h2...h6 ol ul table form`通常用于页面布局，a标签不在其中，可以通过display:block转换为块状元素
                *   inline不单独占一行，高以及宽不可以设置，宽就是他包含文字或图片的宽度，不可改变;如`a span`;除此之外，可用display:inline转换为inline显示;inline元素间有默认间距
                *   inline-block不单独占一行，可以设置高、宽、外边距以及内边距如`img`;可用display:inline-block来转换元素;
            *   元素类型转换 --`display`
        *   浮动定位`float` --改变盒子排列，可以有左浮动和右浮动
            *   float属性`right left none` --图文混排以及多列布局时可以用到;当设定float时，盒子脱离文档流，位置被其他盒子占据;
            *   clear属性`both left right none` --both清楚左右两侧浮动即不能存在浮动元素，如果有要另起一行;left则是左侧;right是右侧;
        *   层定位`position` --上一层盒子覆盖下一层 相对于谁定位`top是盒子距离上面的距离，同理left、right、bottom，z-index谁大谁在上面`
            *   fixed --固定定位`相对于浏览器窗口进行定位 以浏览器左顶点为原点(0,0)`
            *   relative --相对定位`相对于直接父元素进行定位`
            *   absolute --绝对定位`相对于static定位以外的第一个父元素进行定位 relative/absolute/body定位`
            *   static --当前元素在文档流中，没有定位
    *   border-radius --圆角边框`设置两个值：水平方向 垂直方向`
        *   border-top-left-radius --左上角形状
        *   border-top-right-radius --右上角形状
        *   border-bottom-left-radius --左下角形状
        *   border-bottom-right-radius --右下角形状
    *   box-shadow --盒子阴影
        *   inset --水平偏移 垂直偏移 模糊距离 颜色;内部阴影
        *   outset --默认值 外部阴影
    *   文本与文字
        *   text-shadow --水平偏移 垂直偏移 阴影大小 颜色 两个效果：文字描边与浮雕效果
        *   word-wrap --normal break-word:允许长单词、URL强制进行换行
        *   @font-face --定义字体，让用户从服务器下载网页所需要的特殊字体;`@fonts-face{font-family:kastlerFont;
        src:url('./fonts/kastler.ttf'),url('./fonts/kastler.eot')}同样从fonts文件夹里引用对不同浏览器适应的字体`
    *   2D变换 `transform` 平面上对元素进行旋转、缩放、移动、拉伸
        *   rotate(xdeg) --旋转 x为正数则顺时针旋转
        *   scale(x,y) --缩放 x为水平方向缩放倍数 y为垂直方向缩放倍数 若省略，则与x同 0-1缩小 >1放大
    *   过渡效果 `transition` 使元素的某个属性从一个值在指定时间内过渡到另一个值
        *   transition-property --属性名 or all 对哪个属性进行变化 多个属性逗号隔开
        *   transition-duration --持续时间 
        *   transition-timing-function --过渡使用的方法(函数) `linear ease ease-in ease-out ease-in-out`分别是匀速、慢快慢、慢快、快慢、慢快慢
        *   transition-delay
    *   动画 `@keyframes`
        *   animation的属性如下
            *   定义动画 --`@keyframes`规则 将一组静态的图片连接起来，每一幅图片都是keyframe
            *   animation-name --引用动画的名字 自己用`@keyframes`定义动画
            *   animation-duration --持续时间
            *   animation-function --动画速度曲线 与过渡效果的函数一致
            *   animation-paly-state --running or pause 当前动画播放的状态
    *   3D变换
        *   transform-style:preserve-3d
            *   rotateX()
            *   rotateY()
            *   rotateZ()
        *   透视属性`persective`
            *   像素值越小，离舞台越远，反之;
        *   内容、父容器、舞台
            *   父容器 --内容旋转`transform-style:preserve-3d and transform:rotateY(60deg)`
            *   舞台 --内容透视`perspective:100px`
#JavaScript
    *   JavaScript概述
        *   一中运行与JS解释器/引擎中的解释型脚本语言
        *   解释型指运行前是不需要编译的，运行不会检查错误，直到遇错停止
        *   使用场合 --PC、手机、平板、机顶盒
        *   运行环境 --NodeJS以及嵌入内核中的JS解释器
        *   JS组成 --核心`ECAMScript` 文档对象模型`DOM 让JS有能力与网页进行对话` 浏览器对象模型`BOM有能力让JS与浏览器对话`
        *   弱类型语言 --由数据来决定数据的类型
        *   面向对象
    *   基础语法
        *   浏览器内核 --负责页面内容的渲染 `两部分:1内容排版引擎解析`HTML和CSS`2脚本解释引擎解析`JS``
        *   网页嵌入网页方式 --1将JS嵌入在元素的`事件`中 2将JS嵌入在`<script>`标记中 3将JS代码写在外部脚本文件中并引入
        *   语句 --分号表示结束 大小写敏感 英文标点符号 由表达式、关键字、运算符组成
        *   注释 --单行注释// 多行注释/**/ 
    *   变量
        *   内存 --保存程序在运行过程中，所需要用到的数据
        *   变量 --内存中的一段存储空间 变量名是内存空间的别名 变量值是保存在内存空间的数据
        *   变量声明 --`var username; var bookprice=2;`声明过程中，尽量不要省略var，否则声明的是全局变量
        *   变量命名规范 --不允许使用JS的关键字和保留关键字 由字母、数字、下划线以及$组成 不能以数字开头 尽量见名知意 可以采用驼峰命名法`合成词组成时，第一个词小写，第二个词之后每个首字母大写`
        *   变量使用 --`var stuName="小猪佩奇";console.log(stuName);` or `var stuName;console.log(stuName);`变量声明后，未赋值，称之为未经初始化变量，输出undefined or 使用为声明变量`console.log(stuHeight);`结果为错误
        *   变量存取操作 --获取变量的值`var stuName="小猪佩奇";console.log(stuName);document.write(stuName);var newName=stuName;` 保存变量的值`var stuName="小猪佩奇";stuName="yes";stuName=newName;`重新赋值