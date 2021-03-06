﻿# 1 四轴飞行器基本原理

四轴飞行器想要平稳飞在空中，第一步需要知道自身在空中的角度，第二步需要保持这个角度的平稳。第一步称为姿态解算，第二步称为自动控制。

* 姿态：四轴在空中的姿态用三个角度来描述：前后（俯仰）角度、左右（横滚）角度、旋转（偏航）角度。
* 姿态解算：通过一些传感器，测量并计算出上述三个角度的过程。常见的三种方式：DMP、互补滤波、四元数。
* 自动控制：使用自动控制算法，将一个值控制在期望值的技术。一般使用PID算法。PID算法的过程是：将角度的期望值与实际值做差，进行PID计算，将得到的控制量输入给电机。这个过程即是自动控制，可以将四轴角度的实际值跟随期望值。从而保持四轴平衡。

# 2 整体框架

遥控器将角度的期望值发送给四轴，四轴根据姿态检测器件，测量出自身角度的实际值，对两个值做差并进行PID计算，保持四轴平稳。


# 3 程序介绍

* CORE:单片机底层的程序
* DMP:测量姿态的传感器的驱动程序
* HARDWARE:各个模块的驱动程序
* NRF:无线通信模块驱动程序
* STM32F10x_FWLib:单片机底层库
* SYSTEM:驱动程序
* UCOSII:实时操作系统程序
* USER:启动程序



# 4 展示



绘制原理图和PCB


![](https://github.com/zhang555/my_quadcopter/blob/master/1.jpg)



电路板


![](https://github.com/zhang555/my_quadcopter/blob/master/2.jpg)

贴元器件


![](https://github.com/zhang555/my_quadcopter/blob/master/3.jpg)


整体效果


![](https://github.com/zhang555/my_quadcopter/blob/master/4.jpg)





