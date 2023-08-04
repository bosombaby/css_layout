# 一、前言
[CSS 布局 - 学习 Web 开发 | MDN](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/CSS_layout)
CSS 布局是指通过 CSS 样式来控制 HTML 元素在页面中的位置和大小。常见的 CSS 布局方式包括：

1. 盒模型布局：通过设置元素的 width、height、padding、border 和 margin 等属性来控制元素的大小和位置。
2. 浮动布局：通过设置元素的 float 属性来使元素脱离文档流，并根据其在文档中的位置进行浮动布局。
3. 定位布局：通过设置元素的 position 属性和 top、bottom、left、right 等属性来控制元素在页面中的位置。
4. 弹性盒子布局（Flexbox）：通过设置元素的 display: flex 属性和 flex-direction、justify-content、align-items 等属性来控制元素在弹性盒子容器中的位置和大小。
5. 网格布局（Grid）：通过设置元素的 display: grid 属性和 grid-template-columns、grid-template-rows、grid-column、grid-row 等属性来控制元素在网格容器中的位置和大小。

以上这些布局方式都有其特点和适用场景，开发者可以根据实际需求选择合适的布局方式。
# 二、flex布局（常用）
[弹性盒子 - 学习 Web 开发 | MDN](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/CSS_layout/Flexbox)

[Flex 布局语法教程 | 菜鸟教程](https://www.runoob.com/w3cnote/flex-grammar.html)

[深入理解 flex-grow、flex-shrink、flex-basis - 掘金](https://juejin.cn/post/6844904016439148551)

flex-grow、flex-shrink 和 flex-basis 是 CSS 中用于设置 flex item 的三个属性。

- flex-grow 属性指定了 flex item 在 flex container 中的剩余空间中所占的比例。默认值为 0，表示该元素不会在空间充足时增长。
- flex-shrink 属性指定了 flex item 在空间不足时所占的比例。默认值为 1，表示该元素会在空间不足时缩小。
- flex-basis 属性指定了 flex item 在主轴方向上的初始大小。默认值为 auto，表示该元素的初始大小由其内容和其他属性（如 width、height 等）来决定。**优先级max-width/min-width > flex-basis > width > box**
# 三、grid网格布局（常用）

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

![7.png](https://cdn.nlark.com/yuque/0/2023/png/27367619/1691130924520-01ae9c10-54d8-4b6c-bb92-1d758f3970ad.png#averageHue=%23f6f6f6&clientId=u75c96903-a389-4&from=ui&id=uf4596776&originHeight=559&originWidth=1264&originalType=binary&ratio=1.25&rotation=0&showTitle=false&size=52038&status=done&style=none&taskId=u2fe9a059-30a7-429e-a2ff-23669314f41&title=)
![8.png](https://cdn.nlark.com/yuque/0/2023/png/27367619/1691131079683-40c4ca6c-b773-440f-b0ac-f134e1777736.png#averageHue=%23cae4ed&clientId=u75c96903-a389-4&from=ui&id=u28dd7eea&originHeight=461&originWidth=1235&originalType=binary&ratio=1.25&rotation=0&showTitle=false&size=50520&status=done&style=none&taskId=u65045b44-7333-4ebc-8507-74b9e68de60&title=)

让浮动元素包含在盒子内部，扩展盒子高度

```css
.wrapper {
    background-color: rgb(79, 185, 227);
    padding: 10px;
    color: #fff;
}
```

```css
  .wrapper {
      background-color: rgb(79, 185, 227);
      padding: 10px;
      color: #fff;
      overflow: auto;  //清除浮动
  }
```

```css
.wrapper {
    background-color: rgb(79, 185, 227);
    padding: 10px;
    color: #fff;
    /* overflow: auto; */
    display: flow-root;
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
z-index 是 CSS 中用来控制元素层叠顺序的属性。在定位方式为**相对定位（relative）、绝对定位（absolute）和固定定位（fixed）**的元素中，可以使用 z-index 属性来控制元素的层叠顺序。z-index 属性的值越大，元素越靠近顶部，覆盖在其他元素之上。
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


