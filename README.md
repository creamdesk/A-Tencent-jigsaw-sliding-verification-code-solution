# A-Tencent-jigsaw-sliding-verification-code-solution
这是一个对T-Sec 天御 验证码，滑动拼图验证码的一种自动化应对处理方案/This is an automatic solution to T-Sec Tianyu verification code and sliding jigsaw verification code



该项目是对腾讯T-Sec天御验证码，滑动验证码的自动化处理方案。使用Selenium、OpenCV等技术，首先获取验证码的背景图片url，之后下载到本地，使用opencv对下载的图片，进行：
    图像处理：将图片转化为灰度图、应用高斯模糊、边缘检测等。
    特征检测：通过寻找图像中的轮廓来确定缺口的位置。
在使用该代码的时候，一定要注意，下载的图片和网页上的图片大小不一致的问题。网页上的图片与下载的图片相比，可能是放大的，也可能是缩小的。因此一般需要，对opencv计算出来的坐标进行，等比例放大或缩小处理。之后计算，滑块需要移动的距离，对验证码进行处理。


![图片](https://github.com/user-attachments/assets/99c458de-af97-4877-bbae-49c8b77ac158)
