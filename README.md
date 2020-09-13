# Monopoly
Game Monopoly for CS big Homework.

有问题or发现新的注意点请发 Issue，做好了发 Pull request.

[Pull request教程](https://www.zhihu.com/question/21682976)

**main.cpp放在最外部**

**在source下放源文件及类的实现（.cpp,.hpp）**

**在class下放类（.class）**

# 整体大概描述

## 游戏目标：
圈地买房产，剩最后一人没破产or达到回合限制结束。n人胜利仅一人（尽量，如果回合结束时前都一样的话太罕见）

## 设计细节：

### 地图制作：
每一格可以视为一个class node，（不管是不是真的有建筑）。所有node可以组成一个地图map。
+ [ ] 人的表示及重合的处理
+ [ ] 特殊建筑的表示

### 玩家：
玩家可设计成class player
+ [ ] 玩家状态（进监狱？正常？破产？又在监狱又破产？）
+ [ ] 资金不够卖房子（卖哪个？），钱够是否买房子
+ [ ] 是否因卡片而被持续影响？

### 建筑or地标or普通点：
建筑也可在地图上表示为class building:public node；地标可以作为基本的building；具有特殊点的可以作为class specialPosition:public building。
+ [ ] 建筑的状态（空置？被买了，被谁买了？被卖了，被谁卖了？）
+ [ ] class player 和 class node 的互动

### 卡片系统及随机事件：
卡片可以由class card处理，考虑卡片是否随机选择？能否重复选择？是否用完？
+ [ ] card与player的对接
+ [ ] card与node的对接
+ [ ] card与action的对接

### 特殊事件：
由卡片引发，或由玩家引发。待完善。可以单独放在 action.cpp
+ [ ] 破产
+ [ ] 进监狱
+ [ ] 进医院
+ [ ] 游戏开始与结束

