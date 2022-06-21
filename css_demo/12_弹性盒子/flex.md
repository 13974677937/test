## flex (弹性盒、伸缩盒)
> css中的一种布局手段，主要用来代替浮动来完成页面的布局
flex可以使元素具有弹性，让元素跟随页面的大小改变而发生改变
### 弹性容器
要使用弹性盒，必须先将一个元素设置为弹性容器
+ display：flex 设置为块级弹性容器
+ display：inline-flex 设置为行内弹性容器
+ 主轴：元素的排列方向
+ 辅轴：元素排列方向的垂直方向
#### flex-direction 
>指定容器中元素的排列方式
+ row 默认值 元素在容器中水平排列
+ row-reverse 反向水平排列
+ col 纵向排列
+ col-reverse 反向纵向排列
#### flex-wrap
>设置弹性元素是否在弹性元素中自动换行
+ nowrap 默认值 不换行
+ wrap 换行
+ wrap-reverse 元素沿着辅轴方向反向换行
#### flex-flow 
> flex-direction 和 flex-wrap 的简写属性
####  justify-content 
> 如何分配容器的空白空间(主轴元素如何排列)
+ flex-start 元素沿着主轴起点排列
+ flex-end 元素沿着主轴终点排列
+ center 居中排列，空白分布在元素首尾
+ space-around 空白分布到元素两侧
+ space-evenly 空白分布到元素的单侧
+ space-between 空白均匀分布到元素间
#### align-items
> 元素在辅轴上如何对齐
+ stretch 默认值 将元素的长度设置为相同的值
+ flex-start 元素不会拉伸，沿着辅轴起点对齐
+ flex-end 元素不会拉伸，沿着辅轴的终点对齐
+ center 居中对齐
+ baseline 基线对齐
#### align-content
> 辅轴上空白空间分布，可选值与 justify-content 一样
### 弹性元素
弹性容器的子元素是弹性元素（弹性项），一个元素同时是弹性容器和弹性元素
#### flex-grow 
> 指定弹性元素伸展的系数，当父元素有多余的空间时，子元素如何伸展，父元素的多余空间会按照系数比列进行分配
#### flex-shrink 
>指定弹性元素收缩的系数，当父元素的空间不足以容纳所有的子元素时，子元素按照系数比列进行收缩
#### flex-basis
> 元素在主轴上的基础长度，如果主轴横向则指定宽度，纵向指定高度
+ auto 默认值，参考元素自身的高度或宽度
+ 传递具体数值，则以该值为准
#### flex
> flex-grow flex-shrink flex-basis的简写属性
+ initial 默认值 'flex: 0 1 auto' 不可伸长 可以缩减
+ auto 'flex: 1 1 auto' 可伸长 可缩减
+ none  'flex: 0 0 auto' 元素没有弹性
#### align-self
> 用于覆盖当前弹性元素的 align-items， 可选值一样
#### order
> 决定弹性元素的排列顺序
