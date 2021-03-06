# flex布局

## 基本概念

采用Flex布局的元素,称为Flex容器(flex container),简称容器,它的所有子元素自动成为容器成员,称为Flex项目(flex item)

## 容器的属性

+ flex-direction

> flex-direction属性决定主轴的方向(即项目的排列方向)
> flex-direction:row|row-reverse|column|column-reverse;

+ flex-wrap
  
> 默认情况下,项目都排在轴线上,flex-wrap属性定义,如果一条轴线排不下,如何换行
> flex-wrap:nowrap|wrap|wrap-reverse

+ flex-flow

> flex-flow属性是flex-direction属性和flex-wrap属性的简写形式,默认值为 row nowrap

+ justify-content

> justify-content属性定义了项目在主轴上的对齐方式
> justify-content:flex-start|flex-end|center|space-between|space-around
> flex-start(默认值):左对齐,flex-end:右对齐,center:居中,space-between:两端对齐,项目之间的间隔都相等,space-around:每个项目两侧的间隔相等,所以,项目之间的间隔比项目于边框的间隔大一倍.

+ align-items

> align-items属性定义项目在交叉轴上如何对齐
> align-item:flex-start|flex-end|center|baseline|stretch
> flex-start:交叉轴的起点对齐,flex-end:交叉轴的终点对齐,center:交叉轴的中点对齐,baseline:项目的第一行文字的基线对齐,stretch(默认值):如果项目未设置高度或设为auto,将占满整个容器高度

+ align-content

> align-content属性定义了多跟轴线的对齐方式,如果项目只有一根轴线,该属性不起作用
> align-content:flex-start|flex-end|center|space-between|space-around|strech

## 项目的属性

+ order

> order属性定义项目的排列顺序.数值越小,排列越靠前,默认为0

+ flex-grow

> flex-grow属性定义项目的放大比例，默认为0，即如果存在剩余空间，也不放大

+ flex-shrink

> flex-shrink属性定义了项目的缩小比例，默认为1，即如果空间不足，该项目将缩小。

+ flex-basis

> flex-basis属性定义了在分配多余空间之前，项目占据的主轴空间（main size）。浏览器根据这个属性，计算主轴是否有多余空间。它的默认值为auto，即项目的本来大小。

+ flex

> flex属性是flex-grow, flex-shrink 和 flex-basis的简写，默认值为0 1 auto。后两个属性可选。

+ align-self

> align-self属性允许单个项目有与其他项目不一样的对齐方式，可覆盖align-items属性。默认值为auto，表示继承父元素的align-items属性，如果没有父元素，则等同于stretch