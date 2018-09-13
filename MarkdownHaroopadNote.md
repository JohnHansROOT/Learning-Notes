# Markdown之Haroopad学习
[TOC]

##markdown类似简化的html，可以用Html代替markdown
	<table>
		<tr>
			<td>Foo</td>
		<tr>
	</table>

<table>
		<tr>
			<td>Foo</td>
		<tr>
</table>
##标题支持两种格式
- 第一种，下面用===
		This H1
		=======
		
		This H2
		-------

This H1
====

This is H2
---

- 第二种，前面用#
		# This H1
		## This H2

## 区块引用Blockquates
	> This is 
	> adssad

> This is asdasdjakdj
> adasdadasdad
> asdafaf
>
>asdsa
>dsad

###可以在整个段落的第一行加上 >
> Thisadkasjdkajakjdasdajkjdkajdkjsj,
adadadad
asdad
asdada.

> adadadsda
> asada

### 区块引用可以嵌套
> This is fff
> 
>> sadjakdj
>
>adjaksjda


### 区块内可以用其他语法
> ## this is a 标题
>
>1. adsad
>2. sddaa
>- asda
>		return 0; 

## 列表
- 无序列表
+ 加好
* 乘号

- 有序列表

1. 注意有个空格
3. 不受数字影响
0. 看吧，真的不受

* bird

* magic
中间加空行等同于用<p>

1.	akdjaskdjkadjkadjka
	asdjsakda
	adaasda
	
	asdad
	asdadsds
2. dad 
3. 用TAB键或者4个space在前，包含多个段落

*	sadkjaskdjad:
	> Thisis a quate
	> adada
	> asdad

*	this is a code block:
			cout << endl;
			1个Tab键插入代码块
			
1986. wozaichifan
上面出问题了吧，可以转义\.
1986\. wozaichifan

## 代码区块
- 前空行
- 缩进4space or 1 tab

这是一个普通段落

	这是一个代码区块

Here is an an

	tell  apppad
		beep
	asdadad
	代码块持续到没有缩进的一行或文件结尾

&copy;
代码区块中，markdown语法失效，因此可以用于撰写与语法相关的文件

	* 这样都不是列表
	2. 这样也不是列表
	> 这也不是区块引用
	
	***cpp
	这都不是代码
	***

- 另一种带语法高亮的代码框
		```language(e.g cpp)
		your code	
		```

```cpp
#include<iostream>
using namespace std;
int main{
	cout << "hello world!" << endl;
    return 0;
}
```
代码块背景框风格可以在perference中code设置

## 分割线

三个以上的星号，减号，底线建立分割线

----
是不是没看见

_____
看见了吧

*****
这个是不是更明显了

_ _ _
加入空格也行的

## 区段元素
### 链接
都是用[]标记
- 行内式

方括号内是显示文字，圆括号内是链接网址，网址后如果要加title，引号扩起就是

This is [an example](http://baidu.com/ "Title") inline link.

[This link](http://baidu.com/) has no title attribute.

- 参考式
相当于先声明再定义，在链接文字的方括号后再接上另一个方括号，第二个方括号里填入辨识链接的标记，在文件的其他任何地方把链接标记的内容定义出来

This is [an example][id] reference-style link.
[id]:http://baidu.com/ "Title here"

也可以不用链接标记，用空括号，这时链接文字就替代了

This is [Google][]

[Google]:http://google.com


- 自动链接：简短的地址可以直接用<>括起来如
`<http://baidu.com>`

## 强调
星号和底线作为强调标记
- 一个星号
*怎么样*
*哦斜体了*
*hello world*
- 两个星号
__这个怎么样__
__哦，加粗了__
un**belie**ble

忘了说了，两边不能**都**有*空白*哦

直接输出，用反斜线 \*wod\*

## 代码
- 行内小段代码，用反引号包起
use the `printf()` function
两个\``也行哈，更多也行
``cout << endl;``

代码区段内，可以输入html原码而不会被认为是html代码而执行
Please don't use any `<p>` tags.

## 图片也可以哦
和链接差不多，前面是个惊叹号
- 行内式
		![Alt text](/path/to/img.jpg "optional title" )

![Desktop](https://raw.githubusercontent.com/JohnHansROOT/Test/master/Screenshot%20from%202018-08-27%2019-53-14.png "title" "width:550px;heigth:550px")

在title后可指定图片长宽

## 表格
第一行是表头，第二行是控制符，如果加上冒号则可控制对齐，在虚线右边加冒号就是右对齐，两边都加就居中，不加则左对齐
```
| c1 | c2 | c3 |
|---|---|---|
| 2 | 3 | 5 |
| 6 | 9 | 0 |
```

| c1 | c2 | c3 |
|---|---|---|
| 2 | 3 | 5 |
| 6 | 9 | 0 |

## 数学公式，采用了Mathjax扩展

	$$
	\sqrt{x-\beta}+(x-\alpha)^2
	$$

$$
\sqrt{x-\beta}+(x-\alpha)^2
$$

## Tasklist
- [x] 韩文斌
- [ ] 韩文字
- [ ] 韩文章
- [x] 韩文正

## Diagram关系图
采用mermaid扩展
	~~~mermaid
	graph TD;
	A-->B;
	A-->C;
	B-->D;
	C-->D;
	~~~
如下，`graph TD;`表示从上到下，LR则从左至右
~~~mermaid
	graph TD;
	A-->B;
	A-->C;
	B-->D;
	C-->D;
~~~

## Haroopad可以直接写PPT
需要在view中开启presentation mode，撰写文档时，用***分页，就会产生独立的一页PPT

********
 注：本文主要参考<https://www.appinn.com/markdown/>,
 <https://blog.csdn.net/u010613552/article/details/54966413>


