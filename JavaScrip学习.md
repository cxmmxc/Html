#JavaScrip学习
</br></br></br></br></br></br></br>
<!-- 下面是目录部分跳转 -->
<h2> 目录 </h2>
* [1.做好学习JavaScript的准备](#1)
	* [1.1.为什么要学习JS](#1.1)
		* [1.1.1 WHY](#1.1.1)
		* [1.1.2 WHAT](#1.1.2)
		* [1.1.3 HOW](#1.1.3)
	* [1.2.如何插入js](#1.2)
	* [1.3 独立引用js外部文件](#1.3)
	* [1.4 找到你的位置(JS在页面中的位置)](#1.4)
	* [1.5 认识语句和符号](#1.5)
	* [1.6 注释](#1.6)
	* [1.7 变量](#1.7)
	* [1.8 if else语句](#1.8)
	* [1.9 函数](#1.9)
* [2.常用互动方法](#2)
	* [2.1 输出内容](#2.1)
	* [2.2 警告(alert对话框)](#2.2)
	* [2.3 确认(confirm对话框)](#2.3)
	* [2.4 提问(消息对话框)](#2.4)
	* [2.5 打开新窗口](#2.5)
	* [2.6 关闭窗口](#2.6)
* [3.Dom操作](#3)
	* [3.1 认识Dom](#3.1)
	* [3.2 通过 ID 获取元素](#3.2)
	* [3.3 innerHTML 属性](#3.3)
	* [3.4 改变 HTML 样式](#3.4)
	* [3.5 显示和隐藏](#3.5)
	* [3.6 控制类名](#3.6)
<h1 id=1>1 做好学习JavaScrip的准备</h1>
<h2 id="1.1">1.1、为什么要学习JavaScrip？</h2>
<h3 id="1.1.1">1.1.1、你知道，为什么JavaScript非常值得我们学习吗？</h3>
  1. 所有主流浏览器都支持JavaScript。
  2. 目前，全世界大部分网页都使用JavaScript。
  3. 它可以让网页呈现各种动态效果。
  4. 做为一个Web开发师，如果你想提供漂亮的网页、令用户满意的上网体验，JavaScript是必不可少的工具。
<h3 id="1.1.2">1.1.2易学性</h3>
  1. 学习环境无外不在，只要有文本编辑器，就能编写JavaScript程序。
  2. 我们可以用简单命令，完成一些基本操作。
<h3 id="1.1.3">1.1.3从哪开始学习呢</h3>
  1. 学习JavaScript的起点就是处理网页，所以我们先学习基础语法和如何使用DOM进行简单操作。
<h2 id="1.2"> 1.2如何插入JS </h2>
  *  我们来看看如何写入JS代码？你只需一步操作,使用`<script>`标签在HTML网页中插入JavaScript代码。注意， `<script>`标签要成对出现，并把JavaScript代码写在`<script></script>`之间。
`<script type="text/javascript">`表示在`<script></script>`之间的是文本类型(text),javascript是为了告诉浏览器里面的文本是属于JavaScript语言。
如图：![图片](http://img.mukewang.com/52e31ea8000149f406440218.jpg)
<h2 id="1.3">1.3独立引用js外部文件</h2>
* 我们可以把HTML文件和JS代码分开,并单独创建一个JavaScript文件(简称JS文件),其文件后缀通常为.js，然后将JS代码直接写在JS文件中。
![js外部文件](http://img.mukewang.com/52898b400001d04005500266.jpg)

<strong> 注意:在JS文件中，不需要`<script>`标签,直接编写JavaScript代码就可以了。 </strong>
</br>
JS文件不能直接运行，需嵌入到HTML文件中执行，我们需在HTML中添加如下代码，就可将JS文件嵌入HTML文件中:</br>
`<script src="script.js"></script>`</br>
![scrip js](http://img.mukewang.com/52898b6900018aeb05540284.jpg) 
<h2 id="1.4">1.4 找到你的位置(JS在页面中的位置) </h2>
* 我们可以将JavaScript代码放在html文件中任何位置，但是我们一般放在网页的head或者body部分。
* <strong>放在`<head>`部分:</strong>最常用的方式是在页面中head部分放置`<script>`元素，浏览器解析head部分就会执行这个代码，然后才解析页面的其余部分。
* **放在`<body>`部分:**
JavaScript代码在网页读取到该语句的时候就会执行.
![html_js_location](http://img.mukewang.com/52a6ad240001086506440600.jpg)
* **注意:**javascript作为一种脚本语言可以放在html页面中任何位置，但是浏览器解释html时是按先后顺序的，所以前面的script就先被执行。比如进行页面显示初始化的js必须放在head里面，因为初始化都要求提前进行（如给页面body设置css等）；而如果是通过事件调用执行的function那么对位置没什么要求的。 
<h2 id="1.5">1.5 认识语句和符号</h2>
* js就是给浏览器发送命令，告诉需要做的事；
* 格式为：**每一句JavaScript代码格式: `语句`;**
<h2 id=1.6>1.6 注释</h2>
* **单行注释：**在注释内容前面加" // "
* **多行注释：** 以/\*开始，以*/结束
<h2 id="1.7">变量</h2>
* 定义变量关键字用**var**；语法如下：`var 变量`;
* 变量的命名规则：</br>
	1. 变量必须使用字母、下划线(_)或者美元符($)开始。

    2. 然后可以使用任意多个英文字母、数字、下划线(_)或者美元符($)组成。

    3. 不能使用JavaScript关键词与JavaScript保留字。</br>
    
  **注意:**</br>
	1. 在JS中区分大小写，如变量mychar与myChar是不一样的，表示是两个变量。</br>
	2. 变量虽然也可以不声明，直接使用，但不规范，需要先声明，后使用。
<h2 id=1.8>1.8 if else语句</h2>
* 跟Java一样
* **语法：**</br>
		if(条件)
		{ 条件成立时执行的代码 }
		else
		{ 条件不成立时执行的代码 }
<h2 id="1.9">1.9 函数</h2>
* **定义函数的语法：**</br>
		function 函数名()
		{
    		 函数代码;
		}
</br>
**function**是定义函数的关键字
<h1 id="2">2 常用互动方法</h1>
<h2 id="2.1">2.1 输出内容</h2>
* **输出方式：**</br>
	`document.write();`
</br>
可以直接输出到网页上显示；输出字符串同Java的
<h2 id="2.2">2.2 警告(alert对话框)</h2>
* 使用`alert()`实现
* **一般用来调试程序。再点击确定按钮前，无法操作网页** 
</br>
<h2 id="2.3">2.3 确认(confirm对话框)</h2>
* confirm弹出的对话框包含“确定”和“取消”按钮
* confirm的返回值是Boolean，点击确定返回true，点击取消返回false；
<h2 id="2.4">2.4 提问(消息对话框)</h2>
* 弹出样式：（包含一个确定按钮、取消按钮与一个文本输入框）。
* **语法：**`prompt(str1, str2);`
* **参数说明：**str1: 要显示在消息对话框中的文本，不可修改。str2：文本框中的内容，可以修改
* **返回值：**确定：返回文本框的内容；取消：返回null
<h2 id=2.5">2.5 打开新窗口</h2>
* open() 方法可以查找一个已经存在或者新建的浏览器窗口。
* **语法：**`window.open([URL], [窗口名称], [参数字符串])`
* **参数说明：** 
	* **URL：**可选参数，在窗口中要显示网页的网址或路径。如果省略这个参数，或者它的值是空字符串，那么窗口就不显示任何文档。
	*  **窗口名称：**可选参数，被打开窗口的名称。
		*  该名称由字母、数字和下划线字符组成。
		*  "_top"、"_blank"、"_selft"具有特殊意义的名称。
       		_blank：在新窗口显示目标网页
       		_self：在当前窗口显示目标网页
       		_top：框架网页中在上部窗口中显示目标网页
		* 相同 name 的窗口只能创建一个，要想创建多个窗口则 name 不能相同。
		* name 不能包含有空格。
	* **参数字符串：**可选参数，设置窗口参数，各参数用逗号隔开。参数如图：</br>
![参数表](http://img.mukewang.com/52e3677900013d6a05020261.jpg)
<h2 id="2.6">2.6 关闭窗口</h2>
* `widow.close()`关闭本窗口，但是有时候不灵，可以参考[本文](http://www.jb51.net/article/34502.htm)。
* <窗口对象>.close();关闭指定窗口。
如下代码：
		<script type="text/javascript">  
		var mywin=window.open('http://www.imooc.com');  
		//将新打的窗口对象，存储在变量mywin中
		mywin.close();
		</script>
<h1 id="3">3 Dom操作</h1>
<h2 id="3.1">3.1 认识Dom</h2>
* **描述：**文档对象模型DOM（Document Object Model）定义访问和处理HTML文档的标准方法。DOM 将HTML文档呈现为带有元素、属性和文本的树结构（节点树）。
* **先来看看下面代码:**
![代码](http://img.mukewang.com/52e4be610001c67307860420.jpg)
**分解成Dom节点层次图：**
![代码](http://img.mukewang.com/52e4bd0f0001dd8d04830279.jpg)
		HTML文档可以说由节点构成的集合，三种常见的DOM节点:
		
		1. 元素节点：上图中<html>、<body>、<p>等都是元素节点，即标签。
		
		2. 文本节点:向用户展示的内容，如<li>...</li>中的JavaScript、DOM、CSS等文本。
		
		3. 属性节点:元素属性，如<a>标签的链接属性href="http://www.imooc.com"。
**看下面代码:**</br>
		<a href="http://www.imooc.com">JavaScript DOM</a>
![tupian](http://img.mukewang.com/52e4bdb80001064c04480196.jpg)
<h2 id="3.2">3.2 通过ID获取元素</h2>
* **语法：**
		 document.getElementById("id")
**注:获取的元素是一个对象，如想对元素进行操作，我们要通过它的属性或方法。**
<h2 id="3.3">3.3 innerHTML属性</h2>
* **语法：**
		Object.innerHTML
**注意：**
		1.Object是获取的元素对象，如通过document.getElementById("ID")获取的元素。
		2.注意书写，innerHTML区分大小写。
<h2 id="3.4">3.4 改变HTML样式</h2>
* **语法：**
		Object.style.property=new style;
* **基本属性表（property）:**
![属性表](http://img.mukewang.com/52e4d4240001dd6c04850229.jpg)
注意:该表只是一小部分CSS样式属性，其它样式也可以通过该方法设置和修改
<h2 id="3.5">3.5 显示和隐藏</h2>
 *网页中看见的显示和隐藏效果，可通过display属性设置*
* **语法：**
		Object.style.display = value
value取值:
![value值](http://img.mukewang.com/52e4dba5000179da04110095.jpg)
<h2 id="3.6">3.6 控制类名</h2>
* **语法：**
		object.className = classname
* **作用:**
	* 获取元素的class 属性
	* 为网页内的某个元素指定一个css样式来更改该元素的外观

**其实就是更改class的名字来来对应设置CSS的class名字；**