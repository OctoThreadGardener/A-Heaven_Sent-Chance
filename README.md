## 接口协议
YQY 
Peter Lu 

2016/10/9 15:02:53 

### 上位机通信部分
```c
struct status{
    bool GameStatus;//00 待机，01开始，10暂停，11结束
    bool IsMinDamaging;//是否收到少量目标伤害
    bool IsMaxDamaging;//是否收到大量目标伤害
    bool IsControling;//是否正在控制飞机
    bool IsHPUp;//是否正在回血
    bool IsHPDown;//是否正在掉血
    bool IsBorder;//是否出界
    bool IsTargetExist;//目标点是否存在
    Enum TargetColor;//目标点颜色
    Point MyPos;
    Point EnemyPos;
    Point TargetPos;
    Point PlanePos;
    int MyHP;
    int EnemyHp;
    Point PropPos;
    int GameTime;
    Enum PropType;
};
void GetStatus();//每次读取上位机信息,开全局吧
void SendStatus(int x,int y);//选手发送信息
```

### 电机
```c
void Motor(u8 n, int c)
//电机n以c的速度前进
//c -255~255，正数表示正转，负数表示反转
//n 1 or 2,1-left,2-right
//尽量线性
```

### 端口读写
需要明确告知：
- GPIO
    - 已开GPIO
    - 读写方法
- IIC
    - 已开端口
    - 读写方法


### 寻路基本模块
```c
void Stop();//无论之前处于什么状态，停住不动。
//需要内部测试以决定正转or反转

void MoveFront(int sec);//笔直向前走,其实情况不一定是两个电机转速一样。

void TurnRound(double degree);//转一个角度，以顺时针计算
//目前想到的实现方式有三种：1、延时，2、罗盘，3、陀螺仪
//具体用哪个看鲁棒性
```

### 获取当前状态
```c
int GetDirection();//用罗盘或者陀螺仪获取当前小车朝向
bool IsCrush();//是否跟对方小车碰撞
.....
```

### 策略
```c
void GetWholeMap();//遍历地图
.....
```