# HTML聚沙成塔

HTML的知识点又多又散，在此记录，更新。（20200202）

## 0 HTML基础

HTML，即超文本标记语言（**Hyper Text Markup Language**）。

注意，不是编程语言，是标记语言，一套标记标签来描述网页。

**两个概念**：元素和属性。可以这样理解，一个标签就是一个元素，每一个元素有多个属性。

    <img src="w3school.jpg" width="104" height="142" />

上例中，`<img>`是元素，`src`,`width`,`height`是这个元素的3个属性，3个属性的=号后的为该属性的值。

一个网页的html基本布局：

    <!DOCTYPE html>
    <html>
        <head>
            网页的基本属性，标题等
            head标签中的内容不会在网页中显示
        </head>
        <body>
            网页显示的内容
        </body>
    </html>

## 1 head标签

例如：

    <head>
        <meta charset="UTF-8">
        <meta name="description" content="html beginning course">
        <title>About HTML</title>
    </head>

### 1.1 title标签

title标签的作用：

* 定义该网页在浏览器标签栏中的标题
* 作为网页被添加到收藏夹时的标题
* 供搜索引擎搜索，显示在搜索引擎结果的标题

title要能够准确的表达出当前网页的核心内容。

### 1.2 meta标签

meta是非常有用的辅助性标签。

1、name属性：

    1.<meta name=”viewport” content=”width=device-width, initial-scale=1, maximum-scale=1, user-scalable=no”>：在移动设备浏览器上，禁用缩放（zooming）功能，用户只能滚动屏幕。
    2.<meta name=”description” content=””>：告诉搜索引擎，当前页面的主要内容是xxx。
    3.<meta name=”keywords” content=””>：告诉搜索引擎，当前页面的关键字。
    4.<meta name=”author” content=””>：告诉搜索引擎，标注网站作者是谁。
    5.<meta name=”copyright” content=””>：标注网站的版权信息。

    摘自 https://www.jianshu.com/p/179ddc16ef55 缺月楼


2、http-equiv属性：

    1.<meta http-equiv=”Set-Cookie” content=”cookievalue=xxx; expires=Friday,12-Jan-2001 18:18:18 GMT; path=/”>:如果网页过期，那么存盘的cookie将被删除。必须使用GMT的时间格式。
    2.<meta http-equiv='expires' content='时间' >：用于设定网页的到期时间。一旦网页过期，必须到服务器上重新传输。
    3.<meta http-equiv=”Refresh” content=”5;URL”>：告诉浏览器在【数字】秒后跳转到【一个网址】
    4.<meta http-equiv=”content-Type” content=”text/html; charset=utf-8″>：设定页面使用的字符集。
    <meta charset=”utf-8″>：在HTML5中设定字符集的简写写法。
    5.<meta http-equiv=”Pragma” content=”no-cache”>：禁止浏览器从本地计算机的缓存中访问页面内容。访问者将无法脱机浏览。
    6.<meta http-equiv=”Window-target” content=”_top”>：用来防止别人在iframe(框架)里调用自己的页面，这也算是一个非常实用的属性。
    7.<meta http-equiv='X-UA-Compatible' content='IE=edge,chrome=1'> :强制浏览器按照特定的版本标准进行渲染。但不支持IE7及以下版本。如果是ie浏览器就用最新的ie渲染，如果是双核浏览器就用chrome内核。

    摘自 https://www.jianshu.com/p/179ddc16ef55 缺月楼

3、charset属性：

定义文档的字符编码，通常使用"UTF-8"。


## 2 标题、段落、链接

### 2.1 标题

<h1\>到<h6\>，6种等级的标题。

<h1\>标签对SEO有很大影响：

>网站上的所有页面都应包含h1，并且标题应仅在页面顶部显示一次。h1称为HTML标记，用于显示网页的主标题。

>每个页面都应该有一个独特的h1，所有网页都应具有唯一的网页标题，因为每个网页都应包含唯一的内容，确保该h1直接解释了该页面的内容。

>搜索引擎会密切关注h1标签中的关键字。搜索引擎抓取时希望关键词覆盖网页的主要主题，避免使用与页面内容无关的关键字。

### 2.2 段落

常用标签：

<p\><\/p>标签：段落

<strong\><\/strong>标签：字体加粗

<em\><\/em>标签：字体斜体

<br\>标签：插入空行，单标签。

<hr\>标签：插入横线分割行，单标签。


### 2.3 链接

超链接用<a\>标签。

    <a href="http://baidu.com" target="_blank">跳转百度</a>

**href属性**的值是要跳转的目的网址，

href：#，空锚点，回到页面顶端，不刷新页面

href："", 空链接，刷新当前页面

**target属性**

target：_blank，目的网址新打开一个页面，

target：_self，默认，从当前页面直接跳转到目的网址。

其他属性：

    将图像作为链接
    <a href="../img/footer.png" download="../img/footer.png">下载图片</a>

    mailto：会自动检测本机系统是否安装邮箱，如果有就会自动打开邮箱，
    没有则会提示用户选择邮箱或者没提示
    <a href="mailto:1533233@qq.com">发送邮件</a>
    <a href="tel:12345678910">一键拨打电话</a>
    <a href="sms:12345678910">一键发送短信</a>

    摘自：https://www.jianshu.com/p/f51a1d2f9172 可乐Cola

## 3 列表和表格

### 3.1 列表

**无序列表**

ul标签

    <ul>
        <li>HTML</li>
        <li>CSS</li>
        <li>JavaScript</li>
    </ul>

<ul>
    <li>HTML</li>
    <li>CSS</li>
    <li>JavaScript</li>
</ul>

**有序列表**

ol标签

    <ol>
        <li>django</li>
        <li>flask</li>
        <li>tornado</li>
    </ol>

<ol>
    <li>django</li>
    <li>flask</li>
    <li>tornado</li>
</ol>

### 3.2 表格

<table\>标签

表格分表头和表内容，表头：<thead\>， 表<tbody\>，行：<tr\>，每个单格： <td\>

    <table>
        <thead>
            <tr>
                <th>ID</th>
                <th>Name</th>
                <th>Age</th>
                <th>Email</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>1</td>
                <td>John Doe</td>
                <td>20</td>
                <td>johnexample@gmail.com</td>
            </tr>
            <tr>
                <td>2</td>
                <td>Bob Smith</td>
                <td>22</td>
                <td>bobexample@gmail.com</td>
            </tr>
            <tr>
                <td>3</td>
                <td>Lily Green</td>
                <td>24</td>
                <td>lilyexample@gmail.com</td>
            </tr>
            <tr>
                <td>4</td>
                <td>Han Meimei</td>
                <td>26</td>
                <td>meimeiexample@gmail.com</td>
            </tr>
        </tbody>
    </table>

实际上应该很难看的没有任何格式的表，下表的格式是markdown自带的

<table>
    <thead>
        <tr>
            <th>ID</th>
            <th>Name</th>
            <th>Age</th>
            <th>Email</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>1</td>
            <td>John Doe</td>
            <td>20</td>
            <td>johnexample@gmail.com</td>
        </tr>
        <tr>
            <td>2</td>
            <td>Bob Smith</td>
            <td>22</td>
            <td>bobexample@gmail.com</td>
        </tr>
        <tr>
            <td>3</td>
            <td>Lily Green</td>
            <td>24</td>
            <td>lilyexample@gmail.com</td>
        </tr>
        <tr>
            <td>4</td>
            <td>Han Meimei</td>
            <td>26</td>
            <td>meimeiexample@gmail.com</td>
        </tr>
    </tbody>
</table>

## 4 表单

<form\>标签用于为用户输入创建 HTML 表单。

表单能够包含 input元素，比如文本字段、复选框、单选框、提交按钮等等。

表单还可以包含 menus、textarea、fieldset、legend 和 label 元素。

表单用于向服务器传输数据。

详情：https://www.w3school.com.cn/tags/tag_form.asp

例如：

    <form action="xxx" method="POST">
        <input type="text" name="name"> Name
        <br>
        <input type="number" name="age"> Age
        <br>
        <input type="date" name="birthday"> Birthday
        <br>
        <input type="radio" name="sex" value="male"> Male
        <br>
        <input type="radio" name="sex" value="female"> Female
        <br>
        <select>
            <option value="football">Football</option>
            <option value="basketball">Basketball</option>
            <option value="pingpang">Ping Pong</option>
        </select> Favorite sport
        <br>
        <input type="submit" value="Submit" />
        <br>
    </form>

具体如下：

<form action="xxx" method="POST">
    <input type="text" name="name"> Name
    <br>
    <input type="number" name="age"> Age
    <br>
    <input type="date" name="birthday"> Birthday
    <br>
    <input type="radio" name="sex" value="male"> Male
    <br>
    <input type="radio" name="sex" value="female"> Female
    <br>
    <select>
        <option value="football">Football</option>
        <option value="basketball">Basketball</option>
        <option value="pingpang">Ping Pong</option>
    </select> Favorite sport
    <br>
    <input type="submit" value="Submit" />
    <br>
</form>

待续
