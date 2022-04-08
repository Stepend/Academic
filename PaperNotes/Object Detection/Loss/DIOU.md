# Distance-IoU Loss: Faster and Better Learning for Bounding Box Regression

## 出发点 

1.   GIOU收敛慢
1.  一个好的bbox有三个要素：IOU、中心偏移、框的形状(文中用横纵比描述)；这三点应该是经验直觉。

## 总体思路

1.  主要是针对GIOU问题改进，给出了GIOU过程——预测框先增大，出现重叠区，然后GIOU退化为IOU
1.  引入一个距离比来解决预测框先增大这个过程的问题
1. 后面将三要素加入到损失函数

## 个人理解 

1. 收敛速度比GIOU快
2. 由于引入横纵比约束框的形状，所以精确度上更高
3. CIOU过于复杂
4. 仍然存在多对一的情况。