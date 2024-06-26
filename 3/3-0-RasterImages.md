# 光栅图像
大多数计算机图形图像都是通过某种光栅显示器（raster display）呈现给用户的。光栅显示器以像素的矩形阵列显示图像。一个常见的例子是平板电脑显示器与电视，它有一个由小型发光像素组成的矩形阵列，这些像素可以单独设置为不同的颜色，通过混合不同强度的红色、绿色和蓝色光来实现不同的颜色，可以创建任何所需的图像。大多数打印机如激光打印机和喷墨打印机，也是光栅设备。它们是基于扫描的，没有物理像素网格，但图像通过在网格上的选定点沉积墨水来依次铺设。

> 像素（pixel）是 `picture element` 的缩写

> 打印机中的颜色更为复杂，涉及至少四种颜料的混合。

光栅在图像输入设备中也很常见。数码相机包含一个图像传感器，该传感器由一个光敏像素的网格组成，每个像素记录其上落下的光的颜色和强度。台式扫描仪包含一个线性像素阵列，该阵列横扫被扫描的页面，每秒进行多次测量以生成一个像素网格。

> 也许是因为光栅图像非常方便，所以光栅设备非常普遍。

因为光栅在设备中如此普遍，光栅图像是存储和处理图像的最常见方式。光栅图像是一个二维数组，存储每个像素的像素值——通常是以三个数字存储的颜色，分别代表红色、绿色和蓝色。存储在内存中的光栅图像可以通过使用存储图像中的每个像素来控制显示器上一个像素的颜色，从而显示出来。

但我们不会总是以这种方式显示图像。有时需要改变图像的大小或方向、校正颜色，甚至将图像显示在移动的三维表面上。即使在电视中，显示器的像素数量也很少与所显示的图像像素数量相同。这些因素打破了图像像素与显示像素之间的直接联系。最好将光栅图像视为显示图像的设备无关描述，而将显示设备视为接近理想图像的一种方式。

除了使用像素数组外，还有其他描述图像的方法。矢量图像通过存储形状的描述来描述图像——由线或曲线界定的颜色区域——而不涉及任何特定的像素网格。本质上，这相当于存储显示图像的指令，而不是显示图像所需的像素。矢量图像的主要优点是它们与分辨率无关，可以在高分辨率设备上很好地显示。相应的缺点是，在显示之前必须将它们光栅化。矢量图像通常用于文本、图表、机械图纸和其他需要清晰度和精确度的应用，而不需要摄影图像和复杂的阴影。

在本章中，我们讨论光栅图像和显示的基础知识，特别关注标准显示器的非线性特性。当我们在后续章节讨论计算图像时，了解像素值与光强之间的关系的细节至关重要。
> 不然，你必须知道图像中的这些数字实际上是什么意思。