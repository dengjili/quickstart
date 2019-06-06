[返回首页](README.md)


markdown快速了解
============

定了一套简易规则，生成目标html的轻量级标记语言。

标题
--------

Markdown提供两种样式的标题，对应HTML 中 &lt;h1&gt; 到 &lt;h6&gt; 标签

* 一种样式的标题只支持&lt;h1&gt;和&lt;h2&gt;，分别由带有等号（=）和连字符（-）的“减号”创建
* 另外一种样式`#`开头，1-6个数分别代表&lt;h1&gt;-&lt;h6&gt;

markdown例子：

	一级标题
	==================
	二级标题
	-------
	### 三级标题
	###### 六级标题

实际输出：

	<h1>一级标题</h1>
	<h2>二级标题</h2>
	<h3>三级标题</h3>
	<h6>六级标题</h6>
	
段落
----------------
像我们平时一段内容为一段，对应HTML 中 &lt;blockquote&gt; 标签，连续两个回车即可。

markdown例子：

	Now is the time for all good men to come to
	the aid of their country. This is just a
	regular paragraph.
	
	The quick brown fox jumped over the lazy
	dog's back.

实际输出：

	<p>Now is the time for all good men to come to
	the aid of their country. This is just a
	regular paragraph.</p>

	<p>The quick brown fox jumped over the lazy
	dog's back.</p>
	
引用
----------------
显示出引用的标志，段落开头使用 > 符号 ，然后后面紧跟一个空格符号，对应HTML 中 &lt;p&gt; 标签

markdown例子：

	> This is a blockquote.
	> 
	> This is the second paragraph in the blockquote.
	>
	> ## This is an H2 in a blockquote.

实际输出：

	<blockquote>
		<p>This is a blockquote.</p>

		<p>This is the second paragraph in the blockquote.</p>

		<h2>This is an H2 in a blockquote</h2>
	</blockquote>
	
字体
----------------
支持斜体、加粗等，分别对应HTML 中 &lt;em&gt;、&lt;strong&gt;标签

markdown例子：

	Some of these words *are emphasized*.
	Some of these words _are emphasized also_.

	Use two asterisks for **strong emphasis**.
	Or, if you prefer, __use two underscores instead__.

实际输出：

	<p>Some of these words <em>are emphasized</em>.
	Some of these words <em>are emphasized also</em>.</p>

	<p>Use two asterisks for <strong>strong emphasis</strong>.
	Or, if you prefer, <strong>use two underscores instead</strong>.</p>
	
列表
----------------
列表分有序和序列之分，分别对应HTML 中 &lt;ul&gt;、&lt;ol&gt;标签

**无序列表**

无序列表可以使用：`*` 或 `+` 或 `-` 符号


markdown例子：

	*   Candy.
	*   Gum.
	*   Booze.
	
	或
	
	+   Candy.
	+   Gum.
	+   Booze.
	
	或
	
	-   Candy.
	-   Gum.
	-   Booze.
	
所有的例子实际输出：

	<ul>
	<li>Candy.</li>
	<li>Gum.</li>
	<li>Booze.</li>
	</ul>
	
**有序列表**

有序列表使用：数字 与 符号 . 的形式

markdown例子：

	1.  Red
	2.  Green
	3.  Blue


实际输出：

	<ol>
	<li>Red</li>
	<li>Green</li>
	<li>Blue</li>
	</ol>
	
超链接
----------------
markdown对于超链接有两种写法，对应HTML 中 &lt;a&gt;标签

**第一种**  

使用上风格与超链接&lt;a&gt;标签相近

markdown例子：

	This is an [example link](http://example.com/).

实际输出：

	<p>This is an <a href="http://example.com/">example link</a>.</p>
	
其中超链接还有一个title属性可选

	This is an [example link](http://example.com/ "With a Title").

实际输出：
	
	<p>This is an <a href="http://example.com/" title="With a Title">example link</a>.</p>

**第二种**  

引用风格，定义变量，然后引用值，适合超链接数量多

markdown例子：

	I get 10 times more traffic from [Google][1] than from
	[Yahoo][2] or [MSN][3].
	
	[1]: http://google.com/        "Google"
	[2]: http://search.yahoo.com/  "Yahoo Search"
	[3]: http://search.msn.com/    "MSN Search"

实际输出：	

	<p>I get 10 times more traffic from <a href="http://google.com/"
	title="Google">Google</a> than from <a href="http://search.yahoo.com/"
	title="Yahoo Search">Yahoo</a> or <a href="http://search.msn.com/"
	title="MSN Search">MSN</a>.</p>