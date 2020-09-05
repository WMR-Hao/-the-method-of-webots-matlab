# windows10下，webots和matlab联合仿真方法：

* 版本：webots R2020a revision1   		matlab r2018b

## 1、安装C语言编译器：MinGW-w64 C/C++

从官网下载编译器文件：https://cn.mathworks.com/matlabcentral/fileexchange/52848-matlab-support-for-the-mingw-w64-c-c++-compiler-from-tdm-gcc ，路径自定，

在matlab中打开编译器文件路径找到安装文件并安装

## 2、修改launcher.m和allincludes.h文件

参照csdn上的https://blog.csdn.net/weixin_43455581/article/details/104686998博客进行操作：

将 D:\simulation_ware\webots\Webots\lib\controller\matlab 路径下的，launcher.m文件修改

![image-20200904091706221](C:\Users\asus\AppData\Roaming\Typora\typora-user-images\image-20200904091706221.png)

画框处修改为： ==/lib/controller/matlab==  

![image-20200904091720644](C:\Users\asus\AppData\Roaming\Typora\typora-user-images\image-20200904091720644.png)

再修改同路径下的allincludes.h文件：

![image-20200904091728194](C:\Users\asus\AppData\Roaming\Typora\typora-user-images\image-20200904091728194.png)

利用快速替换将  ==../../== 修改为 ==../../../==

![image-20200904091736411](C:\Users\asus\AppData\Roaming\Typora\typora-user-images\image-20200904091736411.png)

![image-20200904091741656](C:\Users\asus\AppData\Roaming\Typora\typora-user-images\image-20200904091741656.png)

## 3、利用测试程序测试是否成功

利用matlab测试程序，路径为：D:\simulation_ware\webots\Webots\projects\robots\kuka\youbot\worlds

当画面运动即联合成功！！！

![image-20200904091913782](C:\Users\asus\AppData\Roaming\Typora\typora-user-images\image-20200904091913782.png)