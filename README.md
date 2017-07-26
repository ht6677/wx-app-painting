# 微信小程序：涂鸦

涂鸦小程序，可以在白板上画画，也可以选择涂鸦照片。可以自由修改画笔宽度、颜色。画画代码位于painting、涂鸦照片代码位于painting2

由于考虑到canvas在小程序中层级最高，因此采用动态调整高度的方法显示底部调整栏。

为了解决涂鸦照片的橡皮擦不会破坏原图，采用先为canvas设置background，在保存时先保存绘制的效果，然后清空canvas先绘制原图，再绘制手绘结果图。（利用canvas输出图片背景可以透明的特性）

兼容性&性能问题：

  1、安卓下涂鸦稍微多一点就会存在卡顿现象，估计是由安卓端使用qq浏览器的x5内核所致，ios上表现正常。

  2、在开发者工具中动态修改画布高度的功能有问题，安卓、ios表现正常。


