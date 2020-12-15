# qt6.0-install-win10
qt6.0-install-win10
# 清华源  
https://mirrors.tuna.tsinghua.edu.cn/qt/official_releases/online_installers/qt-unified-windows-x86-online.exe

# 代理 
qt5.15以后只能在线安装，外网很慢，需要代理。  
## 安装并打开Fiddler5，

## 在Fiddler软件下方快速执行的栏里输入并回车，代理软件自动替换QT下载网址为清华源 
urlreplace download.qt.io mirrors.tuna.tsinghua.edu.cn/qt

# 安装

免费注册用户
安装步骤安装

https://blog.csdn.net/cnchu/article/details/109049845

# 测试
## 基础准备
安装 vulkan-runtime.exe（1.6M），图形界面的运行时驱动，不需要sdk。
## release 
ok

## debug 
Qt+MSVC,DeBug模式下报错：the process was ended forcefully

打开调试器，提示：the cdb process terminated

缺少 ucrtbased.dll，找到本机：
C:\Program Files (x86)\Windows Kits\10\bin\10.0.18362.0\x64\ucrt\ucrtbased.dll

注：因为本机是x64，安装的qt6.0也是x64，故需要64的 ucrtbased.dll：
放置：
E:\App\Qt\6.0.0\msvc2019_64\bin\ucrtbased.dll
