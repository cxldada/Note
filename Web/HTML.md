# HTML

> HTML(Hyper Text Markup Language)超文本标记语言

## 文档结构

```html
<!DOCTYPE html>
<!-- lang="en" 代表当前网页的语言为英文，方便浏览器提示翻译 -->
<html lang="en">
<head>
    <!-- 定义当前网页的编码集 -->
    <meta charset="UTF-8">
    <!-- 专门针对IE浏览器，以高版本的IE浏览器来显示网页 -->
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <!-- 针对移动端布局，开启理想端口 -->
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <!-- 定义网页的关键字，可以用作搜索引擎收录，有利于seo优化 -->
    <meta name="keywords" content="content">
    <!--  定义网页描述 -->
    <meta name="description" content="content">
    <!-- 定义网站作者 -->
    <meta name="author" content="cxl">
    <!-- 定义网页标题，显示在网页标签上 -->
    <title>Document</title>
</head>
<body>
    嘿嘿嘿
</body>
</html>
```

`<!DOCTYPE html>`：代表网页的文档类型，申明浏览器解析网页的解析规则

`<html lang="en">`：根标签，每个网页有且只有一个，lang表示网页显示的语言

`<head>`：代表网页的头部，`title`代表网页的标题，内容会显示在窗口栏上，有利于`seo`优化

`<meta charset="utf-8">`：定义了文档的编码集

`<body>`：代表网页的主体，body主要用户写网页的结构代码和内容

如果不写`doctype`标签那么浏览器默认使用**混合模式**加载，写了则按照内容进行代码解析

## 常用标签

### 文本标签

```html
<h1>
    标题标签
</h1>

<p>
    段落标签
</p>

<span>span标签</span>

<label>label标签</label>

<!-- 粗体标签 -->
<b>粗体</b>
<strong>粗体</strong>

<!-- 斜体标签 -->
<i>斜体</i>
<em>斜体</em>

<!-- 换行标签 -->
<br>

<!-- 分割线标签 -->
<hr>

<!-- 图片标签 -->
<img src="" alt="图标加载失败是的说明文字">
```



### 图片标签

```html
<img src="路径" alt="">
```

### 超链接

```html
#+id 可以跳转到指定页面的指定ID元素
<a href="引用地址" target="点击打开的方式 _self | _blank">a标签</a>
```

### 表格标签

```html
table:
	width: 设置表格的宽度
	height: 设置表格的高度
	align: 设置对齐方式 left，right，center
	bgcolor: 设置背景颜色
	cellspacing: 设置单元格之间的间距
	cellpadding: 设置边框与单元格内容的间距
tr:
	width: 没用
	heigth: 设置整行的高度
td:
	width: 设置单元格宽度
	height: 设置单元格高度
	colspan: 合并单元格-列
	rowspan: 合并单元格-行

<table border="1">
    <tr>
        <td></td>
    </tr>
</table>
```

### 表单标签

```html
<form action="提交的服务器" method="提交方式">
    
    <input type="text" placeholder="提示">

    <input type="radio" name="sex" id="nan"> <label for="nan">男</label>
    <input type="radio" name="sex" id="nv"> <label for="nv">女</label>

    <input type="checkbox" checked> LOL

    <select name="slt">
        <option value="1" selected>a</option>
        <option value="2" selected>b</option>
    </select>

    <textarea cols="10" rows="5"></textarea>

</form>

```

* input
  * text文本框
    * placeholder：提示信息
  * password密码框
  * radio单选框
    * 相同name的radio是同一组
    * label标签的for属性可以实现点击文本即可选中
  * checkbox复选框
    * checked：表示选中
  * button普通按钮，也可以用button标签
  * reset重置按钮，也可以用button标签
  * submit提交按钮，也可以用button标签
* select下拉列表
  * multiple：实现多选
  * option的selected表示选中
* textarea标签
  * cols：一行多少字
  * rows：多少行

### 列表标签

```html
<ul>
    <li>无序标签1</li>
    <li>无序标签2</li>
</ul>

<ol>
    <li>有序标签1</li>
    <li>有序标签2</li>
</ol>

可以相互嵌套
<ol>
    <li>
        有序标签1
        <ul>
            <li>内部无序标签1</li>
            <li>内部无序标签2</li>
        </ul>
    </li>
    <li>有序标签2</li>
</ol>

定义列表
dt关键词
dd解释关键词的文本
<dl>
    <dt>A</dt>
    <dd>第一个</dd>
</dl>
```

### 其他标签

```html
<div>
    布局容器
</div>

<marquee behavior="" direction="">跑马灯标签</marquee>

<iframe src="" frameborder="0">
    框架标签，显示其他网页
</iframe>

<br>

<del>删除线</del>
```

