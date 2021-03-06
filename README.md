[TOC] [toc]
# 飞浆（paddlepaddle) 学习笔记

1 参加飞浆课程： https://aistudio.baidu.com/aistudio/education/group/info/1297

让我更进一步对深度学习对基础概念有了新的认识，希望通过这个平台能学习对越来越好； 

这个课程适合基础薄弱的机器学习方面人群，同时也对paddlepaddle这个框架感兴趣和想要实战的人也是非常好的， 课程循序渐近的学习， 更是有技术大咖视频指导。

21天，实现零基础小白到AI工程师的华丽蜕变
描述
本课程由百度飞桨团队精心打磨，用故事讲原理，用代码讲实现，力求将经典案例及模型掰开揉碎为学员讲解，不论你是零基础小白还是有一定经验，都可以学有所获！

 
## 大纲


课程前言


第一章：零基础入门深度学习



第二章：一个案例吃透深度学习



第三章：深度学习实践应用——计算机视觉



第四章：目标检测YoloV3



第五章：深度学习实践应用——自然语言处理



第六章：情感分类



第七章：深度学习实践应用——推荐系统



第八章：深度学习高阶导入


拓展：【AI实战案例项目集】



最大感触是， 通过动手实践飞浆的应用编程，能逐步将实践和理论相结合，易于理解机器学习，深度学习方面的知识，目前发现是最好的国内实践平台。 我们需要有自己的AI基础设施，那就从飞浆PaddlePaddle 开始！

框架为我们做了什么？

   - 1） 根据开发者自定义代码的前向计算，自动完成后项计算
   - 2） 自动完成迭代中，参数更新
   - 3） 保存及加载模型
   - 4） 工业化实践部署
   - 5） 常规数据集，常用计算的算子
   - 6） 还提供了学习和研究用的算力支持

## 代码示例
---
```
# 该模型运行在单个CPU上
use_cuda = False # 如想使用GPU，请设置为 True
place = fluid.CUDAPlace(0) if use_cuda else fluid.CPUPlace()

# 调用train_program 获取预测值，损失值，
prediction, [avg_loss, acc] = train_program()

# 输入的原始图像数据，名称为img，大小为28*28*1
# 标签层，名称为label,对应输入图片的类别标签
# 告知网络传入的数据分为两部分，第一部分是img值，第二部分是label值
feeder = fluid.DataFeeder(feed_list=['img', 'label'], place=place)

# 选择Adam优化器
optimizer = optimizer_program()
optimizer.minimize(avg_loss)
```
