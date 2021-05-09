# Bootstrap

## 响应式

- 媒体查询
...

## bootstrap布局容器
**使用bootstrap需要为页面内容和栅格系统包裹一个.container或.container-fluid容器，**
- container
  - 响应式布局的容器，固定宽度。
  - 
    | 屏幕尺寸 | 容器宽度 |
    | ----    | ---- |
    | >=1200px| 1170px |
    | >=992px | 970px|
    | >=768px | 750px|
    | 超小屏 | 100% |
- container-fluid
  - 适用流式布局 width:100%
  - 适合单独做移动端开发

## 栅格系统
  **gridsystems也叫网格系统，它是指将页面布局划分为等宽的列，然后通过列数的定义来模块化页面布局**
  **Bootstrap里面container宽度是固定的，但不同屏幕下，container的宽度不同，我们再把container划分12等份**

## 栅格系统使用
  **栅格系统用于通过一系列的行（row）和（column）的组合来创建页面布局，你的内容就可以放入这些创建好的布局中**
  | | 超小屏幕（手机）<768px | 小屏设备（平板）>=768px | 中等屏幕（桌面显示器）>=992px | 宽屏设备（大桌面设备）>=1200px |
  |---- | ---- | ---- | ---- | ---- |
  | .container最大宽度 | 自动（100%）|750px | 970px | 1170px |
  | 类前缀 | .col-xs- | .col-sm- | .col-md- | .col-lg- |
  - 行（row）必须放到container布局容器里面
  - 我们实现列的平均划分需要给列添加 **类前缀**
  - 列（column）大于12，多余的列所在的元素将被作为一个整体另起一行排列
  - 每一列默认有左右15px的padding
  - 可以同时为一列指定多个设备的类名，以便划分不同份数，eg: class = "col-md-4 col-sm-6"
  - 列嵌套:加一个row，可以消除父盒子的padding，高度也会等于父盒子、也可以直接写
  - 列偏移:col-lg-offset-*
  - 列排序：col-lg-push-* & col-lg-pull-*
  - 响应式工具：hidden-sm hidden-md...visible-sm
  
## 实现响应式
  1. 把需要响应式的html写两份，其中一份添加class hidden-* ，另一份添加visible-*
  2. 媒体查询 
   ~~~css
   @media screen and (max-width:991px){
     <!-- 表示不大于992px的屏幕下 -->
     .selector{
       ...
     }
   }
   ~~~