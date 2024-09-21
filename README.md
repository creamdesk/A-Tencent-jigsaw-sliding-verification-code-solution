# A-Tencent-jigsaw-sliding-verification-code-solution
这是一个对T-Sec 天御 验证码，滑动拼图验证码的一种自动化应对处理方案/This is an automatic solution to T-Sec Tianyu verification code and sliding jigsaw verification code




---

### 项目简介：T-Sec 天御滑动拼图验证码自动化解决方案

#### 项目概述
本项目旨在提供一种针对腾讯T-Sec天御滑动拼图验证码的自动化处理方案。通过结合Selenium、OpenCV等多种技术手段，实现对这类验证码的自动识别与解决。

#### 技术实现
本方案主要包括以下步骤：

1. **获取验证码背景图片 URL**：利用Selenium从网页中提取验证码背景图片的URL。
2. **下载图片**：通过URL下载背景图片至本地。
3. **图像处理**：使用OpenCV对下载的图片进行预处理，包括但不限于：
   - 将图片转换为灰度图；
   - 应用高斯模糊以减少噪声；
   - 进行边缘检测以增强特征。
4. **特征检测**：通过OpenCV找出图像中的轮廓，以此确定拼图缺口的具体位置。
5. **坐标调整**：考虑到网页上显示的图片尺寸与下载后的图片尺寸可能存在差异（可能是放大或缩小），需对OpenCV计算得出的坐标进行相应的比例调整。
6. **计算滑块移动距离**：根据调整后的坐标，计算滑块需要移动的距离。
7. **模拟用户操作**：使用Selenium模拟用户点击并拖动滑块，完成验证。

#### 注意事项
在使用该代码时，请特别注意以下几点：
- 下载的图片与网页上显示的图片尺寸可能存在不一致的情况。因此，通常需要对OpenCV计算出的坐标进行等比例放大或缩小处理。
- 要运行代码还需要安装firefox，并且配置Firefox WebDriver。
- 该代码为半成品，一些部分还需要读者自定义。


### Project Description: T-Sec Tianyu Sliding Jigsaw Verification Code Automation Solution

#### Project Overview
This project aims to provide an automated solution for handling Tencent T-Sec Tianyu sliding jigsaw verification codes. By combining technologies such as Selenium and OpenCV, it enables the automatic recognition and solving of these types of verification codes.

#### Technical Implementation
The solution includes the following steps:

1. **Obtain the Background Image URL**: Use Selenium to extract the URL of the background image from the webpage.
2. **Download the Image**: Download the background image to the local machine using the obtained URL.
3. **Image Processing**: Preprocess the downloaded image using OpenCV, including:
   - Converting the image to grayscale;
   - Applying Gaussian blur to reduce noise;
   - Performing edge detection to enhance features.
4. **Feature Detection**: Use OpenCV to identify contours within the image to determine the exact position of the puzzle gap.
5. **Coordinate Adjustment**: Since the dimensions of the displayed image on the webpage may differ from the downloaded image (either enlarged or reduced), adjust the coordinates calculated by OpenCV accordingly.
6. **Calculate Slider Movement Distance**: Based on the adjusted coordinates, calculate the distance the slider needs to be moved.
7. **Simulate User Actions**: Use Selenium to simulate user actions by clicking and dragging the slider to complete the verification.

#### Notes
When using this code, please pay special attention to the following points:
- The dimensions of the downloaded image may not match those displayed on the webpage. Therefore, it is usually necessary to adjust the coordinates calculated by OpenCV proportionally.

![图片](https://github.com/user-attachments/assets/99c458de-af97-4877-bbae-49c8b77ac158)
