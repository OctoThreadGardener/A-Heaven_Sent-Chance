# A-Heaven_Sent-Chance　
## 官方那些事
### 调试
### 技术资料
这块两个队不能一样，PCB的话实在不行就换布线，代码可以混乱混乱，具体的算法简述可以瞎写写

## 硬件
  - 红外对管 目前想法安装在车底 淘宝卖家Risym
  - LED灯（白） 为红外增加亮度，以免小车挡光
  - 电机 要求进行适当的屏蔽（如使用金属网等）
  - 定向陀螺仪（IIC传输协议） 含DMP MPU6050 卖家同上
  - 电子指南针模块（IIC传输协议） HMC5883L 卖家同上
  - 杜邦线
  - 电池
  - 待补充
  
## 抽象
  - 车轮控制抽象 使用[-1,1]之间的浮点数确定每一个轮子的转动方向和转动速度
  - 行进抽象 使用坐标点（或速度空间坐标点）完成行进的实现
  - 状态获取抽象
  - 高层抽象（待补充）
  
## 算法
  - 先跑一遍地图
  - 具体情况具体分析
  - 整体估价函数怎么写？
  
### 没塔
黑白颠倒没什么卵用（倒也不好说）
剩下道具还是可以好好用的
无人机两种状态可以视为+-用A*//?

  - 无人机攻击状态
  - 无人机治疗状态 
  
### 有塔
  - 如果没受到攻击
  - 如果受到攻击
  - 无人机攻击状态
  - 无人机治疗状态
  
整体的情况看起来“良机”没什么用，就是可以对付对付

## 理论计算
  - 先转后走和边转变走的优化问题
  - 首次巡航的数据记录问题


For 18th THEDC

## contributors
- ZeroWeight
- mcfloundinho  
![](https://ws1.sinaimg.cn/large/6af89bc8gw1f8qczc22i9j20k00qot98.jpg)
- <big><big><big><big>DavidYQY</big></big></big></big>![](http://338283.com/uploads/allimg/c151013/1444G3R262G0-BB5.jpg)  
![](https://ws3.sinaimg.cn/large/6af89bc8gw1f8szeo7z1qj20b509qq3b.jpg)
- Archer
- liuyuezhangadam
