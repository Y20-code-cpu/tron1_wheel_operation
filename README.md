# tron1_wheel_ws
轮足机器人操控指令，通过电脑端发送指令  
轮足机器人IP：10.192.1.2  
轮足机器人序列号：WF_TRON1A_469  
<br><br>

## 获取机器人状态指令
  ``` bash
  python3 send.py 10.192.1.2 WF_TRON1A_469 status
  ```
<br>

## 灯光操作指令
  ``` bash
  python3 send.py 10.192.1.2 WF_TRON1A_469 light --effect 1  #设置灯光为红色
  python3 send.py 10.192.1.2 WF_TRON1A_469 light --effect 2  #设置灯光为绿色
  python3 send.py 10.192.1.2 WF_TRON1A_469 light --effect 3  #设置灯光为深蓝色
  python3 send.py 10.192.1.2 WF_TRON1A_469 light --effect 4  #设置灯光为浅蓝色
  python3 send.py 10.192.1.2 WF_TRON1A_469 light --effect 5  #设置灯光为紫色
  python3 send.py 10.192.1.2 WF_TRON1A_469 light --effect 6  #设置灯光为黄色
  python3 send.py 10.192.1.2 WF_TRON1A_469 light --effect 7  #设置灯光为白色
  ```
<br>

## 站起操作指令
  在站起之前，先用遥控器将机器人调整至预备状态  
  进入预备状态后，可选择使用代码或遥控器实现机器人站起  
  ``` bash
  python3 send.py 10.192.1.2 WF_TRON1A_469 stand
  ```
<br>

## 蹲下操作指令
  可使用代码或遥控器实现机器人蹲下  
  ``` bash
  python3 send.py 10.192.1.2 WF_TRON1A_469 sit
  ```
<br>

## 行走操作指令
  行走模式下机器人会缓慢移动  
  ``` bash
  python3 send.py 10.192.1.2 WF_TRON1A_469 walk
  ```
<br>

## 移动操作指令
  x：控制线速度  
  z：控制角速度  
  机器人速度会被限制在 x：3.0 m/s  z：1.5 rad/s  
  如需修改可在SPEED_LIMIT_X & SPEED_LIMIT_Z 中修改上限值  
  ``` bash
  python3 send.py 10.192.1.2 WF_TRON1A_469 move --x 1.0 --z 0.3  #持续以1m/s，0.3rad/s行走
  python3 send.py 10.192.1.2 WF_TRON1A_469 move --x 1.0 --z 0.3 duration 2  #以1m/s，0.3rad/s行走,维持2秒
  ```
<br>

## 身高调整指令
  需在站立模式下使用  
  ``` bash
  python3 send.py 10.192.1.2 WF_TRON1A_469 height --dir up
  python3 send.py 10.192.1.2 WF_TRON1A_469 height --dir down
  ```
<br>

## 紧急停止指令
  ``` bash
  python3 send.py 10.192.1.2 WF_TRON1A_469 stop
  ```
