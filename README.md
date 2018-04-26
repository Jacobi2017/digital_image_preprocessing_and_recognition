# digital_image_preprocessing_and_recognition
all sub-algorithms  for the field of digital image preprocessing and recognition


This contains the following application scenarios:

1 . 人脸特征点检测与跟踪  
2 . 嘴眼睛的轮廓跟踪  
3 . 虚拟化妆  
4 . 文字识别  
5 . 目标跟踪 ，模式识别  
6 . 颜色识别  
7 . 物体识别  
8 . 去水印


algorithms:
**1. 图片相似度 :颜色直方图  color-histogram**  
**2. 图片相似度 :尺度不变特征转换 SIFT ,SURF**  
sift和surf仅是提取图片的特征描述矩阵，之后仍需计算图片间的相似度，  
而由于sift算法获取的图片特征点的数量是不定的，所以在比较两个图片的相似度时 存在矩阵的行数不一致的情况，为计算带来复杂度，
这里对于这种情况，我们使用padding参数来控制:  
padding=False 直接抛弃多余的特征点 不计入总相似度的计算。  
padding=True  特征点多的图片，多余的无法找到最相似特征点的进行 相似度补全  
以下是 不同padding时 相似度计算的结果比较：
![padding=False 比较1](https://github.com/laura-zhang-cn/digital_image_preprocessing_and_recognition/blob/master/sift_sim_padding_False.png)  
![padding=False 比较2](https://github.com/laura-zhang-cn/digital_image_preprocessing_and_recognition/blob/master/sift_sim_padding_False2.jpg)  
![padding=False 比较3](https://github.com/laura-zhang-cn/digital_image_preprocessing_and_recognition/blob/master/sift_sim_padding_False3.jpg) 
  
![padding=True 比较1](https://github.com/laura-zhang-cn/digital_image_preprocessing_and_recognition/blob/master/sift_sim_padding_True.jpg)  
![padding=True 比较2](https://github.com/laura-zhang-cn/digital_image_preprocessing_and_recognition/blob/master/sift_sim_padding_True2.jpg)  
![padding=True 比较3](https://github.com/laura-zhang-cn/digital_image_preprocessing_and_recognition/blob/master/sift_sim_padding_True3.jpg)  
  
**3. 文字识别  ： OCR   pytessoract**

**4. 图像修复去水印 ：TM_CCOEFF**


