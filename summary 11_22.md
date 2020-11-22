### 11月12日学习报告
---
#### 一．如何将喜欢的图片做成UI。

##### 方法一（麻烦）：

1.首先在Assets文件夹中新创建一个Picture文件夹，将自己所喜欢的照片重命名后拖入Picture文件夹中；

2.找到Material文件夹（或者创建一个），右键新建一个Material，在Shader中选择Unlit/Texture，将图片拖入Select窗口中，即可新建一个Material，这样就成功将我们所喜欢的图片导入Unity。
##### 方法二（简单且常规）：
将照片拖入Unity中后，直接改变照片的Sprite（2D and UI），然后拖入image的Source Image即可。

#### 二．如何导入喜欢的字体。
1.首先下载字体；

2.在C盘/Windows/Fonts找到自己的字体，在unity中创建一个Fonts文件夹，把字体拖入，即可。

#### 三．如何将button按钮换成自己喜欢的样式。
1.将自己喜欢样式的图片拖入unity中；

2.找到自己的图片，在Inspector界面中将Texture Type改为Sprite（2D and UI），Apply。

3.将图片拖入Source Image中，完成。（如果颜色不好看，可以调整颜色）

#### 四．创建开始界面，并且要应用自己喜欢的图片。
1.创建Canvas，在Canvas中创建Image（图像，仅支持Sprite类型）；

2.重命名，然后在Material中选择自己喜欢的图片就行了。

#### 五．使图片大小铺满屏幕，并且随着屏幕的大小而变化。
1.找到自己创建的Canvas，在Inspector中找到Canvas Scaler，将UI Scale Mode改为Scale With Screen Size，然后将Reference Resolution改为1920*1080（其他的也可以）；

2.将图片的大小也改为1920*1080，这样就完成了。

#### 六．当僵尸数量过多时，人物会被挤到天上，同时僵尸也会跟着一起飞到天上。
锁定人物与僵尸的y轴即可。（transform.Translate这个方法忽略物理效果）
但这个方法有一个弊端，即y轴固定，所以不能通过y轴向量小于多少而Destroy一个物体。
#### 七.创建很多同类型物体时（如拼接草坪），不要以第一块草坪为父物体，而其他草坪为子物体，这样会导致很多麻烦与bug
正确做法：创建一个空物体GameObject，将所有草坪都拖入GameObject中，这样会防止很多不必要的麻烦。