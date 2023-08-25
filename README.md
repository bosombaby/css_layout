# 一、前言
[CSS 布局 - 学习 Web 开发 | MDN](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/CSS_layout)
CSS 布局是指通过 CSS 样式来控制 HTML 元素在页面中的位置和大小。常见的 CSS 布局方式包括：

1. 盒模型布局：通过设置元素的 width、height、padding、border 和 margin 等属性来控制元素的大小和位置。
2. 浮动布局：通过设置元素的 float 属性来使元素脱离文档流，并根据其在文档中的位置进行浮动布局。
3. 定位布局：通过设置元素的 position 属性和 top、bottom、left、right 等属性来控制元素在页面中的位置。
4. 弹性盒子布局（Flexbox）：通过设置元素的 display: flex 属性和 flex-direction、justify-content、align-items 等属性来控制元素在弹性盒子容器中的位置和大小。
5. 网格布局（Grid）：通过设置元素的 display: grid 属性和 grid-template-columns、grid-template-rows、grid-column、grid-row 等属性来控制元素在网格容器中的位置和大小。

以上这些布局方式都有其特点和适用场景，开发者可以根据实际需求选择合适的布局方式。

**源码地址**：[css布局](https://github.com/bosombaby/css_layout)
# 二、flex布局（常用）
[弹性盒子 - 学习 Web 开发 | MDN](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/CSS_layout/Flexbox)

[Flex 布局语法教程 | 菜鸟教程](https://www.runoob.com/w3cnote/flex-grammar.html)

[深入理解 flex-grow、flex-shrink、flex-basis - 掘金](https://juejin.cn/post/6844904016439148551)

flex-grow、flex-shrink 和 flex-basis 是 CSS 中用于设置 flex item 的三个属性。

- flex-grow 属性指定了 flex item 在 flex container 中的剩余空间中所占的比例。默认值为 0，表示该元素不会在空间充足时增长。
- flex-shrink 属性指定了 flex item 在空间不足时所占的比例。默认值为 1，表示该元素会在空间不足时缩小。
- flex-basis 属性指定了 flex item 在主轴方向上的初始大小。默认值为 auto，表示该元素的初始大小由其内容和其他属性（如 width、height 等）来决定。**优先级max-width/min-width > flex-basis > width > box**
# 三、grid网格布局（常用）
[网格 - 学习 Web 开发 | MDN](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/CSS_layout/Grids)

[Grid Garden](https://cssgridgarden.com/)

[最强大的 CSS 布局 —— Grid 布局 - 掘金](https://juejin.cn/post/6854573220306255880)
# 四、float浮动
[浮动 - 学习 Web 开发 | MDN](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/CSS_layout/Floats)

CSS 中的浮动（float）是一种布局方式，可以使元素脱离文档流，并根据其在文档中的位置进行浮动布局。浮动元素会尽可能地靠近容器的左侧或右侧，并且会尽可能地占据容器中的空间。浮动元素可以通过设置 float 属性来实现。
## 4.1 简单的例子
![4.png](https://cdn.nlark.com/yuque/0/2023/png/27367619/1691130106555-5636e387-09df-469f-b57e-cf1d1e578614.png#averageHue=%23efefef&clientId=u75c96903-a389-4&from=ui&id=ue569d5ed&originHeight=374&originWidth=1134&originalType=binary&ratio=1.25&rotation=0&showTitle=false&size=49503&status=done&style=none&taskId=u776a7743-5459-418d-9336-4bc1d91907f&title=)
```css
.box {
  float: left;
  width: 150px;
  height: 100px;
  border-radius: 5px;
  background-color: rgb(207, 232, 220);
  padding: 1em;
  margin-right: 25px;
}
```
## 4.2 可视化浮动效果

![5.png](https://cdn.nlark.com/yuque/0/2023/png/27367619/1691130460748-5fda6e6b-ca90-4255-ac46-0591fd4ad0b1.png#averageHue=%23f2f2c9&clientId=u75c96903-a389-4&from=ui&id=ua07751f7&originHeight=445&originWidth=1181&originalType=binary&ratio=1.25&rotation=0&showTitle=false&size=49768&status=done&style=none&taskId=u068d32ec-d21c-46a5-8c9b-74571487a8f&title=)
段落并没有被移走，只是文字被浮动的盒子挤到右侧位置。
## 4.3 清除浮动
![6.png](https://cdn.nlark.com/yuque/0/2023/png/27367619/1691130591052-968f90fa-178f-4243-b0a8-54b6cbf9e198.png#averageHue=%23f2f2cb&clientId=u75c96903-a389-4&from=ui&id=uff1e3aec&originHeight=473&originWidth=1160&originalType=binary&ratio=1.25&rotation=0&showTitle=false&size=49508&status=done&style=none&taskId=ua5d853a4-a634-4edc-a4ca-1bd00501bf6&title=)
应该看到，第二个段落已经停止了浮动，不会再跟随浮动元素排布了。clear 属性接受下列值：

- left：停止任何活动的左浮动
- right：停止任何活动的右浮动
- both：停止任何活动的左右浮动
## 4.4 清除盒子浮动
[【小白入门】浮动、清除浮动与BFC - 掘金](https://juejin.cn/post/7216221384371781669)

![3.png](https://cdn.nlark.com/yuque/0/2023/png/27367619/1692001272696-cfdb155e-26bf-4b91-829c-ec715509b45f.png#averageHue=%23e3d7d5&clientId=u0bc1d55f-a171-4&from=ui&id=uf628d3fd&originHeight=492&originWidth=1324&originalType=binary&ratio=1.25&rotation=0&showTitle=false&size=10162&status=done&style=none&taskId=u8039754d-ed9e-4aa1-a6a9-aef47fec0ae&title=)

![5.png](https://cdn.nlark.com/yuque/0/2023/png/27367619/1692001489721-b5c149e8-6aa5-4e3f-b55f-19fc103cb203.png#averageHue=%23cee7db&clientId=u0bc1d55f-a171-4&from=ui&id=u905f3025&originHeight=492&originWidth=1119&originalType=binary&ratio=1.25&rotation=0&showTitle=false&size=9701&status=done&style=none&taskId=u23a94a76-5dcf-4a1b-a948-6b01170ca98&title=)
```html
<div class="wrapper">
  <div class="box">1</div>
  <div class="box">2</div>
  <div class="box">3</div>
</div>

<div class="content">
  content
</div>
```

### 4.4.1 设置父元素高度（不推荐）
![4.png](https://cdn.nlark.com/yuque/0/2023/png/27367619/1692001299678-18436924-4854-4ced-b0f5-48f5afc73f04.png#averageHue=%23cee7db&clientId=u0bc1d55f-a171-4&from=ui&id=uee626c98&originHeight=544&originWidth=1140&originalType=binary&ratio=1.25&rotation=0&showTitle=false&size=10119&status=done&style=none&taskId=u9eb2bb95-30a4-48a0-a6ff-7c963c6ba43&title=)
```css
.wrapper {
      width: 100%;
      height: 200px;
      background-color: skyblue;
      border: 1px solid #ccc;
  }
```
不推荐使用的原因有以下几点：

1. 内容溢出

当子元素的内容超出父元素的高度时，会导致内容溢出，从而影响布局的效果。如果使用固定高度来设置父元素高度，就无法自适应子元素的高度，从而可能导致内容溢出的问题。

1. 响应式布局

在响应式布局中，需要根据不同的设备尺寸来调整布局。如果使用固定高度来设置父元素高度，就无法适应不同的设备尺寸，从而可能导致布局错乱的问题。

1. 维护成本高

当需要修改布局时，如果使用固定高度来设置父元素高度，就需要手动修改高度值，从而增加了维护成本。而如果使用其他布局方式，例如使用 flexbox 或 grid 布局，就可以更方便地进行布局调整。
### 4.4.2 增加子容器（不推荐）
```css
.clear {
   /* 清除左右浮动元素 */
  clear: both;
}
```

```html
<div class="wrapper">
    <div class="box">1</div>
    <div class="box">2</div>
    <div class="box">3</div>
    <div class="clear"></div>
</div>
```

**原因：增加无用标签结构**
### 4.4.3 改变下方受影响元素（不推荐）

![6.png](https://cdn.nlark.com/yuque/0/2023/png/27367619/1692001816165-b981c3da-54a0-4aeb-8f79-6c6875a62e80.png#averageHue=%2339403c&clientId=u0bc1d55f-a171-4&from=ui&id=uc790db36&originHeight=504&originWidth=1119&originalType=binary&ratio=1.25&rotation=0&showTitle=false&size=9768&status=done&style=none&taskId=u837c2051-64c2-4c42-8dad-db923fcd400&title=)
```css
.content {
      width: 500px;
      height: 200px;
      background-color: pink;
      clear: both;
  }
```

**原因：这种方式只能清除上面的浮动，但是浮动元素未撑开父级元素**
### 4.4.4 伪元素
```css
.wrapper::after {
    content: "";
    display: block;
    clear: both;
}
```
### 4.4.5 使用BFC
```css
.wrapper {
    width: 100%;
    /* height: 200px; */
    background-color: skyblue;
    border: 1px solid #ccc;
    overflow: hidden;
}
```
# 五、position定位（常用）
[定位 - 学习 Web 开发 | MDN](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/CSS_layout/Positioning)
## 5.1 静态定位（static）
静态定位（static）是元素的默认定位方式，元素按照其在 HTML 中的顺序进行布局。在静态定位下，元素的位置不会受到 top、bottom、left、right、z-index 等属性的影响，也不会受到其他元素的影响。因此，静态定位的元素会按照其在 HTML 中的顺序进行布局，并且不会脱离文档流。
```css
.positioned {
  position: static;
  background: yellow;
}
```
## 5.2 相对定位（relative）

![9.png](https://cdn.nlark.com/yuque/0/2023/png/27367619/1691133888638-5ccd5d96-2a3f-45ac-b2f8-89a6b0733818.png#averageHue=%23fafa00&clientId=u75c96903-a389-4&from=ui&id=u3ace6648&originHeight=642&originWidth=923&originalType=binary&ratio=1.25&rotation=0&showTitle=false&size=40943&status=done&style=none&taskId=uc0306895-0cad-4838-a5c8-902be09492b&title=)

![10.png](https://cdn.nlark.com/yuque/0/2023/png/27367619/1691134022598-ff928c22-3463-40f7-8442-9093af4ae481.png#averageHue=%23f8f2dc&clientId=u75c96903-a389-4&from=ui&id=u9f10194a&originHeight=854&originWidth=981&originalType=binary&ratio=1.25&rotation=0&showTitle=false&size=47396&status=done&style=none&taskId=u47fbdc03-b44b-4223-9ee5-007cdc22e15&title=)

```css
.positioned {
      position: relative;
      background-color: yellow;
      top: 50px;
      left: 50px;
  }
```

**相对定位（relative）是相对于原本元素在文档流中的位置进行定位的，参照物是元素在文档流中的位置。**

在相对定位下，元素的位置可以通过设置 top、bottom、left、right 等属性来进行微调，但是元素仍然占据其在文档流中的位置，不会影响其他元素的布局。
## 5.3 绝对定位（absolute）

![11.png](https://cdn.nlark.com/yuque/0/2023/png/27367619/1691134563786-3ac5eda5-ddff-43ba-9de2-69f26550b989.png#averageHue=%23f9f4dd&clientId=u75c96903-a389-4&from=ui&id=u2e33d0c7&originHeight=510&originWidth=1780&originalType=binary&ratio=1.25&rotation=0&showTitle=false&size=43328&status=done&style=none&taskId=u6974c83c-c28d-4aac-ac5e-37922a8d35b&title=)


绝对定位（absolute）是相对于元素的最近的已定位祖先元素进行定位的，如果没有已定位的祖先元素，则相对于文档的左上角进行定位。在绝对定位下，元素的位置可以通过设置 top、bottom、left、right 等属性来进行微调，元素会脱离文档流，可能会影响其他元素的布局。

**在绝对定位下，元素会脱离文档流，不再占据原来的空间，因此它的宽度不再受到父元素的限制。**在这个例子中，.positioned 元素设置了 position: absolute，因此它是一个绝对定位的元素，不再占据原来的空间，宽度默认为内容的宽度。由于 .positioned 元素的宽度不再受到父元素的限制，因此它的宽度变成了内容的宽度加上 padding 和 border 的宽度。如果需要设置 .positioned 元素的宽度，可以通过设置 width 属性来进行设置。
## 5.4 层叠关系（z-index）

![12.png](https://cdn.nlark.com/yuque/0/2023/png/27367619/1691134960745-1ecf4a41-5d7c-41d6-bc86-7b39ad5ac712.png#averageHue=%23fbfb00&clientId=u75c96903-a389-4&from=ui&id=ud14e6996&originHeight=597&originWidth=931&originalType=binary&ratio=1.25&rotation=0&showTitle=false&size=41120&status=done&style=none&taskId=u5ba0abcd-3410-4ad3-9068-66ca919d246&title=)
z-index 是 CSS 中用来控制元素层叠顺序的属性。在定位方式为**相对定位（relative）、绝对定位（absolute）和固定定位（fixed）、粘性定位（sticky）**的元素中，可以使用 z-index 属性来控制元素的层叠顺序。z-index 属性的值越大，元素越靠近顶部，覆盖在其他元素之上。
需要注意的是，z-index 属性只对定位元素有效，对于未定位的元素是无效的。
## 5.5 固定定位（fixed）

![13.png](https://cdn.nlark.com/yuque/0/2023/png/27367619/1691135382016-888167cb-80c0-460d-8e95-b105070f5def.png#averageHue=%23d5e309&clientId=u75c96903-a389-4&from=ui&id=u41e7316d&originHeight=357&originWidth=729&originalType=binary&ratio=1.25&rotation=0&showTitle=false&size=25167&status=done&style=none&taskId=u0d8a193e-bedd-40e8-acbe-ec00b6f100d&title=)
固定定位（fixed）是一种定位方式，它可以让元素相对于浏览器窗口固定位置。在固定定位下，元素的位置可以通过设置 top、bottom、left、right 等属性来进行微调，元素会脱离文档流，不会影响其他元素的布局。
## 5.6 粘性定位（sticky）
![14.png](https://cdn.nlark.com/yuque/0/2023/png/27367619/1691135789489-0c6426f5-d676-4e4e-b7ea-3c6b886a0e5e.png#averageHue=%23cdcdcd&clientId=u75c96903-a389-4&from=ui&id=u0618e227&originHeight=537&originWidth=836&originalType=binary&ratio=1.25&rotation=0&showTitle=false&size=10430&status=done&style=none&taskId=udd48048a-88e7-484f-8a55-bbcabcd0f00&title=)

它基本上是相对位置和固定位置的混合体，它允许被定位的元素表现得像相对定位一样，直到它滚动到某个阈值点（例如，从视口顶部起 10 像素）为止，此后它就变得固定了。例如，它可用于使导航栏随页面滚动直到特定点，然后粘贴在页面顶部。
# 六、响应式设计
[响应式设计 - 学习 Web 开发 | MDN](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/CSS_layout/Responsive_Design)
# 七、媒体查询
[媒体查询入门指南 - 学习 Web 开发 | MDN](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/CSS_layout/Media_queries)

CSS 媒体查询（Media Queries）是一种用于针对不同的设备和屏幕尺寸应用不同的样式的技术。使用媒体查询可以让网页在不同的设备上呈现出最佳的显示效果，从而实现响应式设计。


```css
@media media-type and (media-feature-rule) {
  /* CSS rules go here */
}

//简写
@media  (media-feature-rule) {
  /* CSS rules go here */
}
```
它由以下部分组成：

- 一个媒体类型，告诉浏览器这段代码是用在什么类型的媒体上的（例如印刷品或者屏幕）；
- 一个媒体表达式，是一个被包含的 CSS 生效所需的规则或者测试；
- 一组 CSS 规则，会在测试通过且媒体类型正确的时候应用。

media-type 是媒体类型，用于指定媒体查询适用的设备类型。常见的媒体类型包括：

- all：适用于所有设备；
- screen：适用于计算机屏幕、平板电脑、智能手机等；
- print：适用于打印机和打印预览；
- speech：适用于屏幕阅读器等语音合成设备。
# 八、BFC
[区块格式化上下文 - Web 开发者指南 | MDN](https://developer.mozilla.org/zh-CN/docs/Web/Guide/CSS/Block_formatting_context)

[掌握外边距折叠 - CSS：层叠样式表 | MDN](https://developer.mozilla.org/zh-CN/docs/Web/CSS/CSS_box_model/Mastering_margin_collapsing)

[外边距合并和塌陷问题及解决方法_如何解决外边距合并_陈闲之的博客-CSDN博客](https://blog.csdn.net/weixin_50939386/article/details/123603966)
# 十、布局实战
## 10.1 单列
![1.png](https://cdn.nlark.com/yuque/0/2023/png/27367619/1691999621374-c9a7bbbf-f92a-45fb-b3ea-8cde594ba18c.png#averageHue=%2387ceea&clientId=u0bc1d55f-a171-4&from=ui&id=u4ac2ee7b&originHeight=887&originWidth=1521&originalType=binary&ratio=1.25&rotation=0&showTitle=false&size=8926&status=done&style=none&taskId=u2ab84158-e18c-4599-a12e-5f166b34368&title=)

**解释**：一般的块级盒模型，一层层显示
```css
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <style>
        body {
            max-width: 1200px;
            margin: 0 auto;
            background-color: gray;
        }

        header,
        .main,
        footer {
            height: 100px;
            background-color: #fff;

        }

        header {
            height: 10vh;
            background-color: pink;
            margin-bottom: 5vh;
        }

        .main {
            height: 70vh;
            background-color: skyblue;
            margin-bottom: 5vh;
        }

        footer {
            height: 10vh;
            background-color: yellow;
        }
    </style>
    <title>单列布局</title>
</head>

<body>
    <header></header>
    <div class="main"></div>
    <footer></footer>
</body>

</html>
```
## 10.2 双列
![2.png](https://cdn.nlark.com/yuque/0/2023/png/27367619/1691999698293-af58d88e-0946-42b5-a73a-8b8fce40ab13.png#averageHue=%2387ceea&clientId=u0bc1d55f-a171-4&from=ui&id=ud882c0d0&originHeight=887&originWidth=1476&originalType=binary&ratio=1.25&rotation=0&showTitle=false&size=7790&status=done&style=none&taskId=u405e215a-4152-4dbf-802f-f8b49c06c91&title=)

**解释**：双列布局为左侧固定宽度，右侧自适应。一般有四种方法，分别为浮动、定位、flex布局、grid布局
```html
<div class="container">
  <div class="left"></div>
  <div class="right"></div>
</div>
```
### 10.2.1 浮动
```css
.left {
    float: left;
    width: 200px;
    height: 100%;
    background-color: pink;
}

.right {
    margin-left: 200px;
    width: auto;
    height: 100%;
    background-color: skyblue;
}
```
### 10.2.2 定位
```css
.container {
    position: relative;
    width: 100%;
    height: 100vh;
}

.left {
    position: absolute;
    width: 200px;
    height: 100%;
    background-color: pink;
}

.right {
    margin-left: 200px;
    height: 100%;
    background-color: skyblue;
}
```
### 10.2.3 flex布局
```css
.container {
    display: flex;
    width: 100%;
    height: 100vh;
}

.left {
    width: 200px;
    height: 100%;
    background-color: pink;
}

.right {
    flex: 1;
    background-color: skyblue;
    height: 100%;
}
```
### 10.2.4 grid布局
```css
.container {
    display: grid;
    grid-template-columns: 200px 1fr;
    width: 100%;
    height: 100vh;
}

.left {
    height: 100%;
    background-color: pink;
}

.right {
    background-color: skyblue;
    height: 100%;
}
```
## 10.3 三列

![8.png](https://cdn.nlark.com/yuque/0/2023/png/27367619/1692015449939-e247d17c-dc22-471b-b6cd-da42887dbc83.png#averageHue=%23cb8f7b&clientId=u95895104-3f59-4&from=ui&id=u7e6941bd&originHeight=868&originWidth=1790&originalType=binary&ratio=1.25&rotation=0&showTitle=false&size=8151&status=done&style=none&taskId=u2ffe75d6-7f6a-4220-b8e5-357eafe4c4f&title=)
```html
<div class="container">
  <div class="left"></div>
  <div class="right"></div>
  <div class="center"></div>
</div>
```

**解释**：左右两侧固定宽度，中间自适应
### 10.3.1 浮动
```css
.container {
  width: 100%;
  height: 100vh;
  overflow: hidden;
}

.left {
  float: left;
  width: 100px;
  height: 100%;
  background-color: pink;
  display: block;
}

.center {
  background-color: darksalmon;
  margin: 0 100px;
  height: 100%;
}

.right {
  float: right;
  width: 100px;
  background-color: skyblue;
  height: 100%;
}
```

```html
<div class="container">
  <div class="left"></div>
  <div class="right"></div>
  <div class="center"></div>
</div>
```

**注意：布局时需要将center元素写在最后，因为默认中间盒子撑开。如果放在首位，则会让左右两侧浮动元素掉下来**
### 10.3.2 定位
```css
.container {
  position: relative;
  width: 100%;
  height: 100vh;

}

.left {
  position: absolute;
  left: 0;
  width: 100px;
  height: 100%;
  background-color: pink;
}

.center {
  margin: 0 100px;
  height: 100%;
  background-color: darksalmon;
}

.right {
  position: absolute;
  right: 0;
  width: 100px;
  background-color: skyblue;
  height: 100%;
}
```
### 10.3.3 flex布局
```css
.container {
    display: flex;
    width: 100%;
    height: 100vh;

}

.left {
    width: 200px;
    height: 100%;
    background-color: pink;
}

.center {
    flex: 1;
    height: 100%;
    background-color: darksalmon;
}

.right {
    width: 200px;
    background-color: skyblue;
    height: 100%;
}
```
### 10.3.4 gird布局
```css
.container {
    display: grid;
    grid-template-columns: 100px auto 100px;
    width: 100%;
    height: 100vh;

}

.left {

    height: 100%;
    background-color: pink;
}

.center {
    height: 100%;
    background-color: darksalmon;
}

.right {
    background-color: skyblue;
    height: 100%;
}
```
## 10.4 圣杯和双飞翼
[CSS经典三列布局—圣杯布局与双飞翼布局 - 掘金](https://juejin.cn/post/7118571813742837774)

圣杯和双飞翼先加载中间的模块，左右两侧随后加载。布局尽量不使用浮动，可以使用flex或者grid布局，随后用order调整顺序。
## 10.5 居中显示

![9.png](https://cdn.nlark.com/yuque/0/2023/png/27367619/1692061507507-8dae1929-3ba2-476f-b526-10ca46ef9a0d.png#averageHue=%23808080&clientId=u18980514-e2d1-4&from=ui&id=ueeebccd2&originHeight=451&originWidth=651&originalType=binary&ratio=1.25&rotation=0&showTitle=false&size=2202&status=done&style=none&taskId=u19afba1c-a8e9-48c2-b513-af4e62fea93&title=)
[面试官：你能实现多少种水平垂直居中的布局（定宽高和不定宽高） - 掘金](https://juejin.cn/post/6844903982960214029)


