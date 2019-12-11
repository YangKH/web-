# 基本选择器
- 通配符选择器 （0）
```css
	*{
		padding:0;
		margin:0;
	}
```
- 元素(伪元素)选择器（1）
```css
	div{
		padding:0;
		margin:0;
	}
```
- 类(伪类/属性)选择器（10）
```css
	.classname{
		padding:0;
		margin:0;
	}
```
- Id择器（100）
```css
	#idname{
		padding:0;
		margin:0;
	}
```
### style（1000）
```html
	<div style="padding:0;margin:0">JavaScript</div>
```
### !important（至高无上）
```css
	选择器{
		padding:0 !important;
		margin:0;
	}
```
# 组合选择器
- 交集选择器(并且的关系)选择器之间不能有空格
```css
	div.header{
		background: #000000;
	}
```
```html

	<p class="header">
		
	</p>
	<div>1243</div>
	[<div class="header">Test</div>]

- 并集选择器(或者的关系)选择器之间用逗号
```css
	div,.header{
		background: #000000;
	}
```
```html

	[<p class="header"></p>]
	[<div>1243</div>]

- 后代选择器（后代元素，嵌套）至少一个空格逗号
```css
	div .header{
		background: #000000;
	}
```
```html
<div>
	[<p class="header"></p>]
	<h1>[<span class="header"></span>]</h1>
</div>
```
- 子代选择器（子元素，父子嵌套）
```css
	div > .header{
		background: #000000;
	}
```
```html
<div>
	[<p class="header"></p>]
	<h1><span class="header"></span></h1>
</div>
```
- 相邻兄弟选择器（相邻且是兄弟），相邻是指后面的，不含前面的元素。
```css
	div + .header{
		background: #000000;
	}
```
```html
	<p class="header">1</p>
	<div>Test</div>
	[<p class="header">2</p>]
```
## a标签伪类选择器的书写顺序(顺序正确才是达到正常效果)
	a:link
	
	a:visited
	
	a:hover
	
	a:active
# 新增的几个伪类选择器
- 属于其父元素的第一个子元素并且子元素属于选择器
```css
	选择器:first-child{
		
	}
```	
- 属于其父元素的最后一个子元素并且子元素属于选择器
```css	
	选择器:last-child{
		
	}
```
- 属于其父元素的第N个子元素并且子元素满足选择器
```css  
	选择器:nth-child(N){
	
	}
```
- 类似nth-child，不同在于从后面开始计算
```css
	选择器:nth-last-child(2){
		
	}
```
- 属于其父元素并且是第N个选择器元素	
```css	
	选择器:nth-of-type(N){
		
	}
```	
- 属于选择器的第一个字符
```css	
	选择器:first-letter{
		
	}
```
