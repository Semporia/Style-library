# 基于uni-app的简单样式库

## 快速开始

将此文件放入static目录下，并在App.vue的

```html
<style lang="scss"></style>
```

中引入

```css
@import "static/styles/index.scss";
```

至此，就可以在项目中使用此样式库中的样式了。

## 使用方法

### 字体大小

样式库提供了一个类```f-x```，这个x为1-300之间(包含1和300)。

示例

```html
<view class="f-20"></view>
```

这个```.f-20```在样式库的内部样式定义为：

```css
.f-20 {
	font-size: 20rpx;
}
```

### 字重

```css
.fw-small {
  font-weight: 600;
}
.fw-medium {
  font-weight: 700;
}
.fw-large {
  font-weight: 800;
}
.fw-none {
  font-weight: normal;
}
```

### 文字对齐

```css
.tal {
  text-align: left;
}
.tac {
  text-align: center;
}
.tar {
  text-align: right;
}
.tie {
  text-indent: 2em;
}
```

### 内外边距

样式库定义了一套内外边距的类名，类似p-x、p-l-x等，这里的x取值规则如下：

+ 0-600(可以等于600)之间的偶数(双数)
+ 能被5除尽的0-600之间的数，如5，25，50，75等

示例

如果我们想定义```60rpx```的左外边距：

```html
<view class="m-l-60"></viwe>
```

这个```.m-l-60```在样式库的内部样式定义为：

```css
.m-l-60 {
  margin-left: 60rpx;
}
```

以此类推。

### flex布局

样式库尽可能的将flex布局所要用到的样式都列出来，通过组合，可以满足大部分flex布局需求。

示例

```html
<view class="flex-sb"></viwe>
```

可以让该元素内的子盒子左右贴边并上下居中，我们可以用

```html
<view class="flex-sb flex-aifs"></viwe>
```

来重置子盒子在交叉轴上的对齐方式（```.flex-aifs```让子盒子在交叉轴上位于起始位置）。

```html
<view class="flex-vfe"></viwe>
```

可以让该元素内的子盒子在垂直方向处于结束位置，其中```.flex-vfe```把主轴改为了垂直方向，我们同样可以用```.flex-aifs```来重置交叉轴的对齐方式。

更多flex布局样式可以查看```flex.scss```源码。

### 宽高

样式库定义了一套宽高的类名，类似w-x、h-x等，这里的x取值规则如下：

+ 2-1000(可以等于1000)

示例

如果我们想定义```426rpx```的宽：

```html
<view class="w-426"></viwe>
```

这个```.w-426```在样式库的内部样式定义为：

```css
.w-426 {
  width: 426rpx;
}
```

以此类推。

### 宽高百分比

样式库定义了一套宽高百分比的类名，类似w-xp、h-xp等，这里的x取值规则如下：

+ 1-100(可以等于100)

示例

如果我们想定义```66%```的高度百分比：

```html
<view class="h-66p"></viwe>
```

这个```.h-66p```在样式库的内部样式定义为：

```css
.h-66p {
  height: 66%;
}
```

以此类推。

### 行高

样式库定义了一套行高的类名，类似lh-x等，这里的x取值规则如下：

+ 10-1000(可以等于1000)

示例

如果我们想定义```32rpx```的高度百分比：

```html
<view class="lh-32"></viwe>
```

这个```.lh-32```在样式库的内部样式定义为：

```css
.lh-32 {
  line-height: 32rpx;
}
```

以此类推。

### 定位

```css
.pos {
  position: relative;    
}
/* 固定定位 */
.pos-fixed {
  position: fixed !important;
}
/* 粘性定位 */
.pos-sticky {
  position: sticky !important;
}
```

定位位置

示例

```html
<view class=".p-ct"></viwe>
```

这个```.p-ct```在样式库的内部样式定义为：

```css
.p-ct {
  position: absolute;
  left: 50%;
  top: 0;
  transform: translateX(-50%);
}
```

更多定位方式可以查看```pos.scss```源码。
