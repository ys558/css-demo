# grid 网格布局

### 本文参考阮一峰的博客写的：

基础概念如下：
容器(container), 项目(item), 单元格(cell), 网格线(grid line)
具体可以参考阮大神的博客，这里不再赘述：
http://www.ruanyifeng.com/blog/2019/03/grid-layout-tutorial.html

+ 和flex布局的主要区别：
    + flex布局为一个维度的布局，即横向
    + grid布局为两个维度的布局，有横向和纵向两个维度

+ 行内网格元素inline-grid：网格均为块级元素，可将其变为行内元素，可见阮一峰写的例子：[grid](https://jsbin.com/guvivum/edit?html,css,output) 和 [inline-grid](https://jsbin.com/qatitav/edit?html,css,output)

```css
div {
  display: inline-grid;
}
```

**注意，设为网格布局以后，容器子元素（项目）的float、display: inline-block、display: table-cell、vertical-align和column-\*等设置都将失效。**

+ `repeat()` 属性[例子](https://github.com/ys558/css-learn/tree/master/04-grid/01-grid-template-columns_grid-template-rows.html)：

```css
grid-template-columns: repeat(2, 100px 20px 80px);
```

上面代码定义了6列，第一列和第四列的宽度为100px，第二列和第五列为20px，第三列和第六列为80px