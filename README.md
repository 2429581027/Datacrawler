# 任务报告：

•    任选一类图像/视频数据进行爬取

•    观察和分析所爬取数据存在的异常/不均衡问题

•    选用合适的方法进行筛选

•    撰写任务报告并上传，提交报告链接；上传个人代码到github，提交项目地址

报告内容：

  任务目标，数据源，爬取方式，数据观察结果，筛选目标，筛选方式，筛选结果

项目内容：

  有Readme文档，内容包括所需运行库、代码运行方式、注意事项

 ## 任务步骤

1． 使用Image-Downloader对dog的图片进行爬取；

2． 配置

1）下载相应python packages

```
pip install pyqt5

pip install future

pip install PySocks

pip install requests

pip install selenium
```

2）  查看谷歌浏览器版本: 版本 96.0.4664.45（正式版本）；

3）下载相应版本得浏览器应用[link](https://chromedriver.chromium.org/downloads)，并将应用放到bin文件价下；

4)）运行 

​	```python image_downloader_gui.py ```

5）遇到错误：AttributeError: type object 'DesiredCapabilities' has no attribute 'PHANTOMJS'

修改：crawler.py中dcap = dict(DesiredCapabilities.PHANTOMJS)为

dcap = dict(DesiredCapabilities.CHROME)，再次运行正常；

3. 下载数据

![img](file:///C:/Users/ZHUHAI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image002.jpg)

![img](file:///C:/Users/ZHUHAI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image004.jpg)



4. 数据筛选：

​    1）. 初级数据筛选：基于图像尺寸和梯度的数据筛选，目的是删除尺寸过小以及空白或过于模糊的图片；

![img](file:///C:/Users/ZHUHAI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image006.jpg)

​    2）. 高级数据筛选：T-SNE，UMAP；

T-SNE：

![img](file:///C:/Users/ZHUHAI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image008.jpg)

UMAP：

![img](file:///C:/Users/ZHUHAI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image010.png)

可以看到以下图片与数据集中的大多数图片确实有较大不同

![img](file:///C:/Users/ZHUHAI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image012.jpg)![img](file:///C:/Users/ZHUHAI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image014.jpg)
