#
## **第三次课堂总结**
>### 图像处理部分

#### **线性滤波**
* 方框滤波
* 均值滤波
* 高值滤波
* 中值滤波
* 双边滤波
#### **膨胀腐蚀**
形态学操作是基于形状的一系列图像处理操作。OPENCV为进行图像的形态学变换提供了快捷的函数。最基本的形态操作有两种，膨胀和腐蚀
* 获取自定义核并通过imshow显示原图
* 创建轨迹图，通过拖动滑动条来改变膨胀和腐蚀的效果
* 调用一个名为**on_TrackbarNumChange()**的函数和**on_ElementSizeChange()**的函数分别用作开关的开关和内核的回调函数
* 效果如图![](media/31.PNG)
  
#### **漫水填充**
* 通过cvtcloor留一份原图的灰度图
* 创建窗口显示原图
* 创建滑动条**(createTrackbar)**控制阈值，以此切换模式
* 初始化阈值回调函数并调用此函数
* 最后更新效果图并显示，效果图如下![](media/32.PNG)

>### **core组建进阶**
访问图像中的像素图像矩阵的大小取决于所用的颜色模型，如果是灰度图像，矩阵如图
![](media/33.PNG)

**感兴趣区域ROI**

在图像处理中,我们常常需要设置感兴趣区域(**ROI,region of interest**),来专注或者简化工作过程.也就是从图像中选择一个图像区域,这个区域是图像分析所关注的重点。我们圈定这个区域,以便进行进一步处理.而且,使用ROI指定想读入的目标,可以减少处理时间,增加精度,给图像处理带来不小的便利

　　在Ｃ++中定义ROI区域有三种方法:

1---使用表示矩形的**Rect  **  
2---使用**range **   
3--OpemCv1.中的**setImageROI()**函数

#### **ROI图像叠加&图像混合**
* 使用immread方法读入原图片，本体和logo
* 定义一个MAT并为其设定ROI区域，为之后叠加做准备
* 加载掩模也就是logo图
* 将logo图复制到创建的ROI区域内
* 将结果图用imshow显示出来，结果如图![](media/34.PNG)
