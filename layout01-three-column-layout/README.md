Three Column Layout (三栏式布局)
==============================

## 绝对定位布局：
* 分析：
![绝对定位布局](https://github.com/fishnon/css-layout-demo/raw/master/layout01-three-column-layout/img/implement-01.png)
* 源码位置：[点击查看](https://github.com/FishNon/css-layout-demo/blob/master/layout01-three-column-layout/basic-demo/implement-one.html)
* 效果查看：[点击查看](https://fishnon.github.io/css-layout-demo/layout01-three-column-layout/basic-demo/implement-one.html)

## 浮动布局：
* 分析：
![浮动布局](https://github.com/fishnon/css-layout-demo/raw/master/layout01-three-column-layout/img/implement-01.png)
* 源码位置：[点击查看](https://github.com/FishNon/css-layout-demo/blob/master/layout01-three-column-layout/basic-demo/implement-two.html)
* 效果查看：[点击查看](https://fishnon.github.io/css-layout-demo/layout01-three-column-layout/basic-demo/implement-two.html)

**注意，绝对定位与浮动定位的主要区别为定位的方式的不同：**
* 绝对定位布局主要是将左右两部分的```position```设置为```absolute```，然后设置中间元素的```margin```来定位中间元素；
* 浮动定位布局主要是将左右两部分分别左右浮动，左元素设置```left：0```，右元素设置```right:0```，左右元素均设置```top:0```，然后设置中间元素的```margin```来定位中间元素；

## 圣杯布局(不带padding)：
* 分析：
![圣杯布局(不带padding)](https://github.com/fishnon/css-layout-demo/raw/master/layout01-three-column-layout/img/implement-02.png)
**HTML 代码分析**
```
<div class="container">
    <div id="main" class="column">Main</div>
    <div id="left" class="column">Left</div>
    <div id="right" class="column">Right</div>
</div>
```
**CSS 代码分析**
```
body{
    min-width : (2X + Y)px;
}
.container{
    padding-left : Xpx;
    padding-right : Ypx;
}
.column{
    position : relative;
    float : left;
}
#center{
    width : 100%;
}
#left{
    width : Xpx;
    margin-left : -100%;
    right : Xpx;
}
#right{
    width : Ypx;
    margin-right : -Ypx;
}
/*兼容IE6，样式前加星号的内容作用于IE6、IE7*/
*html #left{
    left : Ypx;
}
```
* 源码位置：[点击查看](https://github.com/FishNon/css-layout-demo/blob/master/layout01-three-column-layout/basic-demo/implement-three.html)
* 效果查看：[点击查看](https://fishnon.github.io/css-layout-demo/layout01-three-column-layout/basic-demo/implement-three.html)

## 圣杯布局(带padding)
* 分析：
![圣杯布局(带padding)](https://github.com/fishnon/css-layout-demo/raw/master/layout01-three-column-layout/img/implement-03.png)
**HTML 代码分析**
```
<div class="container">
    <div id="main" class="column">Main</div>
    <div id="left" class="column">Left</div>
    <div id="right" class="column">Right</div>
</div>
```
**CSS 代码分析**
```
body{
    min-width: 2(2x + X + 2y)+(2z + Y) + 4mpx;
}
.container{
    padding-left: (2x + X +2m)px;
    padding-right: (2z + Y + 2y + 2m)px;
}
.column{
    position: relative;
    background: #eee;
    float: left;
}
#main{
    padding: 0 ypx;
    width:100%;
}
#left{
    width:Xpx;
    padding: 0 xpx;
    margin-left: -100%;
    right:(X + 2x + 2m +y)px;
}
#right{
    width:Ypx;
    padding: 0 zpx;
    margin-right:-(Y + 2z + 2m)px;
    left:mpx;
}
```
* 源码位置：[点击查看](https://github.com/FishNon/css-layout-demo/blob/master/layout01-three-column-layout/basic-demo/implement-four.html)
* 效果查看：[点击查看](https://fishnon.github.io/css-layout-demo/layout01-three-column-layout/basic-demo/implement-four.html)

## 双飞翼布局：
* 分析：
![双飞翼布局]()
* 源码位置：
[]()
* 效果查看：
[点击查看]()
