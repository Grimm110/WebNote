# HTML

#### WEB技术的分类

---

  **静态WEB技术(客户端技术)**：任何人任何时间访问内容都是一样的——运行于客户端

​       HTML/CSS/JS/图片/音频/视频/Flash....

  **动态WEB技术(服务器端技术)**：不同人不同时间访问内容可能不同

​								—— 一般都需要访问数据库——运行于服务器端

​       PHP/JSP/ASP.NET/Node.js...

​     ![1534214707786](C:\Users\vip班\AppData\Local\Temp\1534214707786.png)



#### 网页中常用的图片格式

---

(1) **JPG/JPEG**：色彩丰富，适用于风景/人物照片，只能是矩形的，不支持透明

(2) **PNG**：色彩不如JPG丰富，但是支持透明，适用于图标、按钮

(3) **GIF**：色彩不如JPG丰富，支持透明但不如PNG好，支持动画，适用于小型的页面动图

(4) **ICO**：用于网页的标题栏中显示的小图标



#### 常用的转义字符

---

`&nbsp;`       英文空格

`&lt; `           小于号 LessThan

`&gt;`           大于号 GreaterThan

`&reg;`          ®

` &trade; `      ™

` &times; `      ×



HTML中标签的两大分类 —— 小重点

---

**(1)行内/内联元素**：inline，可以与其他内容共处一行中

​       b、i、u、s、sub、sup、a、span ....

**(2)块级元素**：block，必须独自占一整行   

​       h1~h6、p、pre、div ....



#### 相对地址和绝对地址

---

**(1) 相对路径**

基于当前页面所在路径查询目标资源对应的相对路径值，如

​       f.jpg   ./f.jpg       img/f.jpg        ./img/f.jpg      ../f.jpg     ../../f.jpg    ../img/f.jpg

**(2) 根绝对路径**

基于当前WEB服务器的根目录查找目录资源的路径值(与当前页面所在地址无关)，

以 `/` 开头——`/` 指代网站的根目录，即 http://127.0.0.1:8080/

​       **/**yy/day01/img/f.jpg

**(3) 绝对路径**

直接以协议名开头的路径地址(与当前页面所在地址无关)

​       \<img src="http://tmooc.cn/script/img_active/1523500894092.jpg">

​       \<img src="https://www.baidu.com/img/bd_logo1.png">



#### 网页中超链接的几种形式

---

  \<a href="./9.html">相对地址</a>

  \<a href="/9.html">根绝对地址</a>

  \<a href="http://127.0.0.1/9.html">绝对地址</a>

--------------------------------------------------

  \<a href="flower.rar">文件下载</a>

  \<a href="mailto: lwh@tedu.cn">联系管理员</a>

  \<a  href="tel: 13501234567">给我打电话</a>

  \<a href="javascript: alert('当前还不能关闭')">关闭窗口</a>

--------------------------------------------------

  \<a name="锚点名称"></a>

  \<a href="#锚点名称">跳转到当前页面的特定位置</a>



#### 表格

---

+ **标记** 

  表格标记： \<table>\</table>

  行：       \<tr>\</tr>       table row

  列/单元格: \<td>\</td>       table data

+ **属性**

  - table 属性
    - border : 设置表格的边框
    - width : 设置表格的宽度
    - height : 设置表格的高度
    - align：设置表格水平对齐方式 取值：center/left/right
      - bgcolor : 背景颜色
      - cellpadding : 设置单元格内边距(边框与内容之间的间距)
      - cellspacing : 设置单元格外边距(边框与边框之间的间距)
    - tr 属性

        - align: 设置当前行内容的水平对齐方式|取值：left/center/right
        - bgcolor: 设置当前行的背景颜色
        - valign: 设置当前行内容的垂直对齐方式|取值：top/middle/bottom
  -  td 属性

      - bgcolor: 单元格的背景颜色

      - width: 宽度

      - height: 高度

      - align: 水平对齐方式

      - valign: 垂直对齐方式

      - colspan: 跨列

      - rowspan: 跨行


##### 不规则表格的使用

+ 跨列：colspan

​       从指定单元格的位置开始，横向向右合并（包含自己），被合并掉的单元格，要删除

+ 跨行：rowspan

​       从指定单元格的位置开始，纵向向下合并（包含自己），被合并掉的单元格，要删除

##### 可选标记

+ 表格的标题

  \<caption>标题\</caption>

  如果设置表格的标题，则必须位于<table>下第一个子元素位置处

+ 行/列标

​      \<th>\</th>

​	所有的td都可以用th替换

+ 表格的复杂应用

  行分组

  - 表头行

  ​        \<thead>\</thead>

  ​	表格中最上面一行进行分组的话，可以放到表头行中

  - 表主体行

    \<tbody>\</tbody>

    表格中间若干行放在tbody中，进行统一管理

  - 表尾行。

  ​        \<tfoot>\</tfoot>
  	表格中最后一行要进行分组的话，可以放在tfoot中

  - 表格嵌套

    表格中所有的被嵌套的内容只能放在td中



#### 列表

---

+ 列表的作用

  按照从上到下的（从左到右）方式来显示所有的数据，并且可以在数据前增加显示的标识。

+ 列表的组成

  列表都是由"列表类型"和"列表项"来组成

+ 列表类型：

  有序列表：\<ol>\</ol> (order list)

  无序列表：\<ul>\</ul> (unorder list)

+ 列表项：

  用于表示列表中的数据（嵌套在列表中类型）

  标记：\<li>\</li> (list item)

##### 列表属性

1) 有序列表属性

+ type 

  作用：指定列表的排序类型

  取值：

  ​	1 数字，默认值

  ​	a 小写字母 

  ​	A 大写字母

  ​	I 大写罗马数字

  ​	i 小写罗马数字

+ start

  作用：指定起始编号是从第 几 个位置开始

  取值：数字

2) 无序列表属性

+ type

  作用：指定列表的标识类型

  取值：

  ​	disc   实心圆

  ​	circle 空心圆

  ​	square 实心方块

  ​	none   不显示标识

3) 列表嵌套

在一个列表中去嵌套另一个列表，被嵌套的列表只能出现在li中

语法：

```html
<ol>
	<li>
		内容
    <ul>
			<li>内容</li>
		</ul>
	</li>
</ol>
```

**自定义列表**

定义列表常用于一类事物的定义或名称解释说明。

语法

1.\<dl>\</dl> 表示定义列表

2. \<dt>\</dt> 表示定义列表中要解释说明的名词

3.\<dd>\</dd> 表示定义列表中对名词解释的内容

使用场合

​      图文混排，或名词解释时使用



### 表单

---

+ 作用

  + 提供可以与用户交互的可视化控件
  + 收集用户信息并提交给服务器

+ 表单的组成

  + 前端部分

  ​            表单控件，与用户交互的可视化控件

  + 后端部分

  ​             对提交数据的处理，xxx.php

+ 表单

  标记：\<form>\</form>

  属性：

  - ##### action

    作用：定义表单被提交时发生的动作，通常定义的是服务器上处理程序的地址（url）,默认提交给本页。

  - ##### method

    作用：指定表单数据的提交方式（方法）

    取值：

     - get (默认值)
       1. 明文提交，待提交的数据会显示在地址栏上
       2. 安全性较低
       3. 提交数据有大小限制，限制为2kb
       4. 向服务器要数据时，使用get方式
    - post
      1. 隐式提交，提交的数据不糊显示在地址栏上
      2. 安全性较高
      3. 提交数据无大小限制
      4. 要传递数据给服务器时，使用post方式
    - put (一般情况禁用)
    - delete(一般情况禁用)

  - ##### enctype

    作用：指定表单数据的编码格式，允许将什么样式的数据提交给服务器

    取值：

    - application/x-www-form-urlencoded

      默认值，允许将任意字符提交给服务器（文件除外）

    - multipart/form-data

      允许将文件提交给服务器

    - text/plain

      只能是普通字符提交给服务器

+ 表单控件

  能够与用户进行交互的可视化控件

  - 分类

  		  1. input元素

  		  2. textarea 多行文本域元素

  		  3. select和option 选项框

  		  4. 其它元素

  + input元素

    作用：在页面中提供各种输入控件，如：文本框，密码框，单选按钮，复选框...

    语法

    ​	标记：\<input>或\<input/>

    ​	属性：

    ​	       1. type 指定创建输入控件的类型

    ​	       2. name 为控件定义名称，服务器端使用（必须的）

    ​	       3. value 控制的值，服务器端使用

    ​	       4. disabled 禁用控件，不能操作并且不能提交，该属性无值，只要出现在标记中，就是禁用

    ​	详解
    	      1. 文本框和密码框

    ​	        	文本框：\<input type="text">

    ​			密码框：\<input type="password">

    ​		属性：

    ​		  1. maxlength 指定限制输入的字符数

    ​		  2. readonly 只读，只能看，但不允许修改，允许提交给服务使用(无值属性)

    ​		  3. placeholder 占位符，即默认显示在控件上的文本

  + 按钮

    1. 提交按钮：\<input type="submit">

       功能：将表单中的数据，提交给服务器上指定的程序（action）

    2. 重置按钮：\<input type="reset">

    ​        功能：将表单的内容恢复到初始化的状态

    3. 普通按钮：\<input type="button">

    ​        没有功能

    ​	属性：value 定义按钮上的文字

  + 单选框和复选框

    1. 单选按钮：\<input type="radio">

    2. 复选框：\<input type="checkbox">

       属性：

       checked 设置默认被选择中，无值属性

       name 除了定义控件名称之外，还能起到分组的作用

  + 隐藏域和文件选择框

    1. 隐藏域：\<input type="hidden">

    ​        想要提交给服务器使用，但是不想展示给用户看的数据可用放在隐藏域中

    2. 文件选择框：\<input type="file">

    ​        提供文件选择按钮

    ​	注意：

    ​	  1.method属性必须为post

    ​	  2.enctype的值必须为multipart/form-data

+ textarea元素

  ​    1.作用

  ​      允许录入多行数据的文本框

  ​    2.语法

  ​      标记：\<textarea>\</textarea>

  ​      属性：

  ​          1.name：定义控件名称，提供给服务器使用

  ​	  2.readonly：只读，无值属性

  ​	  3.cols：指定文本域的列数（设置宽度），即一行能显示多上个英文字符（中文减半）

  ​	  4.rows：指定文本域的行数，即默认显示多上行的数据，超出rows的话会出现滚动条

+ 选项框

  标记：\<select>\</select> 

  作用：在页面中表示一个选项框

  属性：

      1. name 定义选项框的名称，提交给服务器使用
        
      2. size 定义显示选项的数量，默认值为1；如果取值大于1，元素则表现为滚动列表

​          3. multiple 设置多选，无值属性。只有滚动列表支持多选。

​	子标记：\<option>\</option>

​		作用：选项框中具体选项

​		属性：

​			value 定义选项的值 

​			selected 设置默认被选中，无值属性

+ 其它元素

  + label元素

    作用：关联文本域表单控件

    语法：\<label>文本\</label>

    属性：for  用于设置该元素关联表单控件的id值。

  + 为控件分组

  ​      标记：\<fieldset>\</fieldset>   为控件分组

  ​            	 \<legend>\</legend>     为分组指定标题

+ 浮动框架

  作用：允许在一个网页中，再引入另外一个网页。

  语法

  标记：\<iframe>\</iframe>

  属性：

  1. src 要引入网页的url地址
  2. width 宽度
  3. height 高度
  4. frameborder 浮动框架的边框，默认值为1

##### 新表单元素

---

什么是新表单元素

​    在HTML5版本中新提出的控件

详解

1. 电子邮件类型

   作用：表单提交时，会验证数据是否符合email的规范 （@）

   语法：\<input type="email">

2. 搜索类型

​      语法：\<input type="search">

​      作用：提供了快速清除的功能

3. url类型

​      作用：提交时，验证数据是否符合url的规范（绝对路径http://xxx）

​      语法：\<input type="url">

4. 电话号码类型

​      作用：在移动端设备中，显示效果为“拨号键盘”

​      语法：\<input type="tel">

5. 数字类型

​      作用：只能接受数字，并可以灵活调整数字的值

​      语法：\<input type="number">

​      属性：

​          1.value 控件的值

​	  2.min   能接受的最小数字 

​	  3.max   能接受的最大数字

​	  4.step  每次调整数字时数字的变化范围

6. 范围类型

​      作用：提供一个滑块组件，允许用户选取指定范围的值

​      语法：\<input type="range">

​      属性：

​         1.min   范围最小值

​	 2.max   范围最大值

​	 3.step  范围的步长

​	 4.value 初始值

7. 颜色类型

​      作用：提供一个颜色拾取器

​      语法:\<input type="color">

8. 日期类型

​      作用：提供一个日期控件

​      语法：\<input type="date">

9. 月份类型

​      语法：\<input type="month">

​      作用：提供一个月选取控件

10. 周类型

​      语法：\<input type="week">

​      作用：提供一个周选取控件