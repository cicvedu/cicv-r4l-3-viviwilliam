### 作业1


<img width="561" alt="屏幕截图 2024-07-20 013322" src="https://github.com/user-attachments/assets/74d96f39-3dd2-4b4c-a5f2-752ea2691591">

<img width="560" alt="屏幕截图 2024-07-20 013455" src="https://github.com/user-attachments/assets/fc0b6f17-1272-4beb-b4f3-cfc0a0d80735">

<img width="939" alt="屏幕截图 2024-07-20 014223" src="https://github.com/user-attachments/assets/3fb80cd0-62c1-4d62-a57e-a4340cdc4f5b">


### 作业2

**Q: 在该文件夹中调用make LLVM=1，该文件夹内的代码将编译成一个内核模块。请结合你学到的知识，回答以下两个问题：**

1、编译成内核模块，是在哪个文件中以哪条语句定义的？

Kbuild中的:

```bash
obj-m := r4l_e1000_demo.o
```

2、该模块位于独立的文件夹内，却能编译成Linux内核模块，这叫做out-of-tree module，请分析它是如何与内核代码产生联系的？

编译驱动模块的Makefile中使用M=$(PWD)来指定内核模块所在路径,从而构建树外模块.



步骤

1.运行

bush ./build_image.sh

<img width="439" alt="屏幕截图 2024-07-20 214037" src="https://github.com/user-attachments/assets/a2dab7c1-3be6-4119-9bce-35e4a11e3803">


2.运行

insmod r4l_e1000_demo.ko  
ip link set eth0 up  
ifconfig eth0 broadcast 10.0.2.255  
ip addr add 10.0.2.15/255.255.255.0 dev eth0   
ip route add default via 10.0.2.1  
ping 10.0.2.2  


<img width="420" alt="屏幕截图 2024-07-20 214512" src="https://github.com/user-attachments/assets/66600863-08f2-4257-8e2d-d7aef7dcfdb3">



### 作业3
<img width="538" alt="屏幕截图 2024-07-22 210907" src="https://github.com/user-attachments/assets/73d946db-c22f-4f11-822b-50a19c7ecacd">
<img width="504" alt="屏幕截图 2024-07-22 205555" src="https://github.com/user-attachments/assets/c93a200e-d955-421a-8da6-24dc6b9877c2">
<img width="454" alt="屏幕截图 2024-07-22 205918" src="https://github.com/user-attachments/assets/073b5030-bb99-4ff4-a8e0-edb7e505e681">


