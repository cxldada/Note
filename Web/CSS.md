 

# CSS

> CSS（cascading style sheets）层叠样式表

## 书写方式

### 内联样式

直接在HTML标签的style属性中书写

```html
<div style="color: red;">
    a
</div>
```

### 内部样式

在head标签内的style标签中书写

```html
<html>
    <head>
        <style>
            div {
                color: red;
            }
        </style>
    </head>
    <body>
        <div>
            a
        </div>
    </body>
</html>
```

### 外部样式

在head标签中添加link标签来引用外部样式

```html
<html>
    <head>
        <link rel="stylesheet" href="css文件路径">
    </head>
    <body>
        <div>
            a
        </div>
    </body>
</html>

-- div.css --
div {
	color: red;
}
```

### 优先级

一个原则：离标签越近权重越大

## 选择器

### 标签选择器

通过标签名找到指定的标签

### 类选择器

通过标签上的class属性找到相应的标签。

相同的选择器，后面的会盖住前面的

```css
.class_name1[.class_name2] {
    color: red
}
```

### ID选择器

通过标签的ID属性找到标签

### 优先级

ID选择器 > 类选择器 > 标签选择器

## 背景样式

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        div{
            color: red;
            width: 400px;
            height: 100px;
            /* 设置边框 宽度 类型 颜色 */
            border: 1px solid red;
            /* 设置背景颜色 单词 #十六进制比 rgb(r,g,b) */
            background-color: red;
            /* 设置背景图片 url(图片链接或路径) 默认平铺 图片会覆盖背景颜色属性*/
            background-image: none;
            /* 设置背景图片的平铺方式 repeat repeat-x repeat-y no-repeat*/
            background-repeat: repeat;
            /* 
            设置背景图片位置
            单词 left right center bottom 可以填两个词
            x,y轴
                像素
                百分比
             */
            background-position: 0%;
            /* 设置背景图片的大小 
            contain: 一边铺满，另一边不管
            cover: 两边都铺满
            x,y轴：一个值表示宽度，两个值表示宽高
            */
            background-size: auto;
            /* 设置背景图片是否固定 
            scroll: 随滚动条滚动
            fixed：不随滚动条滚动
            */
            background-attachment: scroll;
            /* 复合属性 /前面表示图片位置 /后面表示图片大小 */
            background: pink url(http:baidu.com) no-repeat 50% 50% /100px 100px fixed
        }
    </style>
</head>
<body>
    <div>牛逼</div>
</body>
</html>
```

## hover

```css
鼠标移入事件，会继承变化前的属性
div:hover {
    
}
```

## 文本样式

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        h1 {
            color: red;
            text-align: center;
            /* 设置文本方向 */
            direction: rtl;
        }
        p{
            text-align: right;
            line-height: 100%;
            /* 文本修饰 underline下划线 line-through删除线 overline上划线 none无 */
            text-decoration: underline;
            /* 字符间距 以字符为分割 */
            letter-spacing: 10px;
            /* 字间距 以空格为分割 */
            word-spacing: 10px;
            /* 首行缩进 */
            text-indent: 20px;
            /* 设置字母大小写 */
            text-transform: lowercase;
            /* 设置文本方向 */
            direction: rtl;
        }
        .box{
            width: 200px;
            height: 100px;
            border: 1px solid red;
            text-align: center;
            line-height: 100px;
        }
    </style>
</head>
<body>
    <h1>要下暴雨了</h1>
    <p>三、打卡学习有奖励。
为激励大家学习，即日起，凡是连续完成学习并在此视频下方评论区打卡满15天者（请另外自行开贴否则无效），将获得蜗牛学苑本门课程一阶段原创（电子）教材，打卡30天获得二阶段教材，打卡45天获得三阶段教材，打卡60天获得四阶段教材。
PS：由于参加活动的小伙伴较多，各位打卡挑战完成，请私聊小蜗，核对无误后将按照顺序依次给出权限。（不要一个劲儿催，催更慢……）

四、蜗牛学苑是一家怎样的IT培训机构？
1、全程面授。绝不会为了节约教学成本而推行视频或者双元教学。
2、最低大专学历方可入读，硬性门槛，不接受协商。不会为了赚钱来者不拒，当然不是我们看不起学历低的学生，只是你们来学习成功的几率真的太低，试错成本太高，这也是为你们负责。
3、校区直营。我们最在乎的是品牌形象和学生认可度，绝不为了赚快钱搞什么品牌加盟割韭菜。目前在成都、重庆、西安、上海、武汉、深圳等城市均开设有直营校区。
4、课程体系及时更新。我们设立专门的课程研发中心，课程保持半年一小更新，一年一次大更新的节奏，尽可能紧跟目前企业所需。
5、一周免费试学，中途不满意可以随时办理退学和退费。不存在入学就不退、超过多少时间不退、退费难的问题。想退就退，解决后顾之忧。
6、公司设有专门的研发部门，同时我司参股的研发公司雷人科技也会一直提供技术支持，保证教学中有真实开发项目案例。
7、合同制保障就业并且保证最低薪资，没达标退还三倍差价，课程学完66个工作日未就业全额退费，通过试用期才算就业成功，且保证工作性质。
8、学员可以自主的选择求职身份。我们的培养目标是让学员具备解决企业实际问题的能力，而不是靠忽悠面试官，所以我们不但不强制学员进行简历包装，而且还鼓励学生走培训简历，我们要让更多的企业认识和认可我们出去的学员，慢慢摘掉培训机构和培训生身上的“水货”标签。sldkfap
        asdkjfapwjfas
        faskdfjpasdjf
        akwpjfad
    </p>
    <div class="box">
        文本样式
    </div>
</body>
</html>
```

## 行内标签

* 用于组织文本内容
* 特点
  * 共享一行
  * 不支持宽高，由内容决定

### 块级标签

* 用于组织布局
* 特点
  * 独占一行，不能和其他标签在同一行显示
  * 支持宽高

### 行内块级标签

* 特点
  * 可以同行显示
  * 支持宽高

### 行和块相互转换

```css
dispaly: block; /* 转为块 */
display: inline-block; /* 行内块 */
display: inline; /* 转为行内元素 */
```

