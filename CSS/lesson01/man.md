扩展: 外部样式两种写法
链接式:
html
<!-- 外部样式 -->
<link rel="stylesheet" href="./css/style.css>

导入式:
css2.1
<!-- 导入式 -->
<style>
    @import url("./css/style.css");
</style>

2, 选择器
作用: 选择页面上的某一个或者某一类元素

2.1 基本选择器
1, 标签选择器
2: 类选择器 class
3: id 选择器

3: 美化网页元素
3.1: 为什么要美化网页
1. 有效的传递页面信息
2. 美化页面, 页面漂亮
3. 凸显页面的主题
4. 提高用户体验

span标签: 重点要突出的字使用span

3.3: 文本样式
1. 颜色 color rgb rgba
2. 文本对齐方式 text-alight=center
3. 首行缩进 text-indent: 2em
4. 行号 line-height: 
5. 装饰 test-decoration:
6. 文本图片水平对齐: 
<!-- 水平对齐~ 参照物, a, b-->
    <style>
        img, span{
            vertical-align:middle;
        }
3.4 阴影

3.5 超链接伪类
正常情况下, a, a:hover
a{
            text-decoration: none;
            color:darkgray
        }
        /* 鼠标悬浮的颜色 (只需记住 hover) */
        a:hover{
            color: orange;
            font-size: 10px;
        }
        /* 鼠标按住未释放的状态 */
        a:active{
            color: olivedrab;
        }


3.6 列表

3.7. 背景

背景颜色

背景图片
13 00:09:58

4: 盒子模型

4.1 盒子什么是盒子模型

margin: 外边距

padding: 内边距

border: 边框

## 4.2 边框
1 边框的粗细
2 边框的样式
3 边框的颜色

## 4.3 外边距

盒子的计算方式: 你这个元素到底多大?

margin + border + padding + 内容宽度

50*50

## 4.4 圆角边框
4个角


## 4.5 盒子阴影



## 5.1 浮动
1. 标准文档流

块级元素: 独占一行
```
1. h1~h5 p div ... 列表
```

行内元素: 不独占一行
```
1. span a img strong ...
```

含内元素可以被包含在块级元素中, 反之, 则不可以~

## 5.2 display
1. 这个也是一种实现行内元素排列的方式, 但是我们很多情况都是用 float

## 5.3 float


```
1. 左右浮动 flaot
```

## 5.4 父级边框塌陷的问题
clear
/*
clear: right; 右侧不允许有浮动元素
clear: left; 左侧不允许有浮动
clear: both; 两侧不允许有浮动
clear: none; 两侧不允许有浮动元素
*/

## 解决方案:
1: 增加父级元素的高度~
#father {
    border: 1px #000 solid;
    height: 800px;
}

2: 增加一个空的div标签, 清除浮动
<div class="clear"></div>
.clear {
    clear: both;
    margin: 0;
    padding: 0;
}

3. overflow
在父级元素中增加一个 overflow: hidden;

4. 父类添加一个伪类: after
#father:after{
    content: '';
    display: block;
    clear: both;
}

## 小结:
1. 浮动元素后面增加空的div
    简单, 代码中尽量避免空div

2. 设置父元素高度
    简单, 元素假设有了固定的高度, 就会被限制

3. overflow
    简单, 下拉的一些场景避免使用

4. 父类添加一些伪类: after(推荐)
    写法稍微复杂移动, 推荐使用

## 5.5 对比
display 
 方向不可控制
float
 浮动起来的话会脱离标准文档流, 所以要解决父级边框塌陷的问题~

## 6 定位
## 6.1 相对定位
相对定位: 
position: relative;
相对于原来的位置, 进行偏移, 相对定位的话, 它仍然在标准文档流中! 原来的位置会被保留
top: -20px
left: 20px
bottom: -10px
right: 20px;

## 6.2 绝对定位
定位: 基于xxx定位, 上下左右~
1. 没有父级元素定位的前提下, 相对于浏览器的定位
2. 假设父级元素存在定位, 我们通常会相对于父级元素进行偏移~
3. 在父级元素范围内移动
    相对于父级或浏览器的位置, 进行指定的偏移, 绝对定位的话, 它不在在标准文档流中, 原来的位置不会被保留


## 6.3 固定定位 fixed




## 6.4 z-index
图层~
z-index: 默认是0, 最高无限999

## 7 动画
自己百度

## 8总结

