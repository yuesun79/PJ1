# PJ设计文档

> 孙悦	学号：18307110426
>
> Github地址：https://github.com/yuesun79
>
> Github Pages地址：https://yuesun79.github.io/PJ1/



## 项目完成情况

***如果没有疏漏的话，项目应该是全部完成了的***

***下面补充一些小的 tips（与部分功能相关）***



### 登录页

> index.html
>
> 点击上方注册可以切换到注册页
>
> 点击登录按钮进入首页（目前不输入用户名与密码也可以跳转）

### 注册页

> register.html
>
> 点击上方登录可以切换到登录页
>
> 点击注册按钮进入登录页（目前不输入用户名、E-mail、密码也可以跳转）

### 首页

>home.html
>
>照片展示部分：**将鼠标移至相应图片上方（hover状态），显示标题和描述**。
>
>脚注：**鼠标移至微信图标上方，显示微信二维码**。
>
>高清头图`background-attachment: fixed;`
>
>导航栏样式、写入home.css,需要导航栏的页面都会引入home.css。

### 浏览页

>browser.html
>
>左侧边栏中的**搜索栏**点击后出现**搜索”GO“按钮**，进行搜索。

### 搜索页

> search.html
>
> 图片及描述部分

### 上传页

> upload.html
>
> 上传预览

### 我的页

>collections.html
>
>图片及描述部分格式与搜索页相同，故引入search.css

### 收藏页

>favorates.html
>
>图片及描述部分格式与搜索页相同，故引入search.css

### 详情页

>detail.html



## BONUS

### 更复杂的图片处理

>虽然我的方法不复杂，但是貌似解决了这个问题，如下：
>
>下述为**home**页的图片处理方法：
>
>```
>.main figure{
>     width: 300px;
>     height: 300px;
> }
>.main figure img{
>    width: 100%;
>    height: 100%;
>    object-fit: cover;
>}
>```
>
>下述为**search**页的图片处理方法：
>
>```
>.result img {
>    width: 230px;
>    height: 230px;
>    object-fit: cover;
>    border-radius: 25px;
>    margin: 0 30px 30px 30px;
>}
>```
>
>方法可以说是一样的：为img图片设置一个限定它的长宽，然后声明`object-fit: cover;`
>
>**`object-fit`** [CSS](https://developer.mozilla.org/zh-CN/docs/Web/CSS) 属性指定[可替换元素](https://developer.mozilla.org/zh-CN/docs/Web/CSS/Replaced_element)的内容应该如何适应到其使用的高度和宽度确定的框。
>
>**`cover`**被替换的内容在保持其宽高比的同时填充元素的整个内容框。如果对象的宽高比与内容框不相匹配，该对象将被剪裁以适应内容框。
>
>***虽然解决的方法很简单，但是好像解决了大问题***:joy:

### 响应式布局

> * `<meta name="viewport" content="width=device-width">`
>
> 为响应式Web设计设置网页**首先**在`<head>`区`<title>`上面加入**上述代码**：告诉本该缩小网页的移动浏览器，不要缩小，让页面宽度匹配手机显示器的真实宽度即可。

>* **布局大多使用`display: flex;`**
>
>在需要布局的父辈元素css中写入上述css样式，根据各自网页的布局情况选择**`flex-box`**横纵向排布和是否空间不够时换行显示，通过**`justify-contect`**调整flex布局的显示是居中、分散、靠左或右等等，**能够实现大部分的响应式布局**。

>* **媒体查询**
>
>方法：调节浏览器显示区域大小，记录整体布局开始错位、崩塌的宽度，可以作为媒体查询节点的备选项，并且特别注意一些特殊节点，如：设备宽度由笔记本宽度到平板电脑宽度再到手机宽度时的节点变化。
>
>使用`@media (max-width: Xpx) and (min-width: Ypx) {...}`对细节进行更加精准的布局。

### 界面美观

> 到网页看看吧～





