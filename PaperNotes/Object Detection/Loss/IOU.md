# UnitBox: An Advanced Object Detection Network

## 出发点 

1.  在此之前对坐标回归都是用的$L_2$损失，基于的假设是bbox参数相对独立
2.  直觉上讲bbox的参数不是独立的，应该联合考虑，IOU顺理成章被提出(这里不清楚是IOU指标先出来，还是有了IOU后才有IOU指标，估计是指标先出来)

## 总体思路

1.  $L_2$损失在坐标回归上的假设不合适，目标的坐标不应该独立考虑，因该有一定的关联
1. 通过IOU将坐标的关联联合起来
1. 实验证明这个想法是可靠的

## 个人理解

1.  直觉驱使实验、实验得出现象、多次实验总结结论
1.  缺少理论分析，典型的工程思维
1.  直觉很重要，IOU算是坐标回归的一次突破，机会总是给有准备的人。
1.  实现细节没必要看的，不同的bbox的定义方式实现不太一样，思想是相同的