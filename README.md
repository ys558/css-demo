## css3 笔记:
---
基础, 代码在[这里](https://github.com/ys558/css-demo/tree/master/01_base)

### 1. 选择器:
#### 1.1 后代选择器: 即使多层嵌套也行
语法: 空格

示例代码:
```css
  div p {}
```

### 1.2 子代选择器: 即使多层嵌套也行, 和1.1后代选择器类似, 但效率比后代选择器高
语法: >

示例代码:
```css
  div > p {}
``` 

### 1.3 紧邻选择器:
语法: +

示例代码: 
```css
  /* 紧挨着div的下面一个p标签 */
  div + p {}
```

### 1.4 紧邻之后的所有元素的选择器
语法: ~

示例: [01_css3的样式选择器.html](./01_css3的样式选择器.html): 
```css
  /* 紧挨着strong的所有a标签 */
  strong~a { }
```
## 2. 属性选择器
语法: []

示例代码:[02_css3属性选择器.html](./02_css3属性选择器.html)
```css
	/* 属性: */
  a[href=a2] { }
  div[align=center] { }

  /* class中有含有dd的 */
  [class|=dd] {}
  
  /* 正则的扩展:*/
  a[href *=image] {}
  a[href $=jpg] {}
```

## 3. 伪类伪元素选择器
### 3.1 伪类:
语法: :

示例代码: 一般只用在a标签
```css 
	a:link {}
	a:visited {}
	a:hover {}
	a:active {}
```

### 3.2 伪元素
语法: ::

示例代码: [03_结构性伪类选择器1.html](./03_结构性伪类选择器1.html)
```css
  p::first-line { }

  /* 在p标签前插入 "你好" 的内容*/
  p::before { content: "你好" }

  /
```

### 4. 结构性伪类:

示例代码: [03_结构性伪类选择器1.html](./03_结构性伪类选择器1.html)
```css
  /* 表示根节点 */
  :root {}

  /* ul子代li.不含class为three的那个li */
  ul > li:not(.three) {}

  /* li 中没有内容的隐藏 */
  li:empty { display: none;}

  /* 只用作a标签点击后的锚点: */
  :target { font-size: 1rem; }
```

[css动画基础](https://github.com/ys558/css-demo/tree/master/02_css_animation_base)

[ToolTips组件及原理](https://github.com/ys558/css-demo/blob/master/03_Component_demo/tooltips.html)