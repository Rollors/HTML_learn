# HTML_learndas
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
    *   div
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