# mtcnn
### （多任务层叠卷积神经网络框架）
## 问题点解读：
1. 根据什么设置的IoU对比阈值？        阈值的设置是需要做大量的比对测试得到的最有值，当然也可以直接使用现有神经网络相关论文中推理提供的阈值。
2. NMS在mtcnn的三层网络中是否只在R-Net和O-Net中执行？       不是的    NMS是在三层网络中都有参与计算输出 face classfication、 boundingbox location （left up & right dowm）、 landmark location (left & right eye  nose left & right mouse)
3. 如果没有boundingbox相交的情况是如何设置阈值的？  没有相交的情况不存在NMS计算
4. mtcnn三层网络是如何分布执行的？ 每个网络做了哪些工作？   
