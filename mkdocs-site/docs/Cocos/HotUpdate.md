
# 热更新
python 本地http服务器

```
python -m http.server --bind 192.168.31.147 10086 --directory E:\Cocos\ZhaoChenHui\hot-update
```
/data/app:
这是用户通过应用商店或手动安装的应用程序的默认存储位置。你可以使用文件管理器或adb shell来查看和管理这个目录下的应用程序。  
/system/app:
这个目录通常包含由手机厂商预装的系统应用程序。这个目录通常需要root权限才能访问和修改。  
data/data/<包名>:
每个应用程序在安装后都会在`/data/data`目录下创建一个私有目录，用于存储应用程序的数据和配置信息。这个目录只有应用程序本身和具有root权限的用户才能访问  



# 逆向

Root Explorer 安卓文件浏览  
https://www.mumuplayer.com/en/games/productivity/root-explorer-on-pc.html

## frida
```
pip isntall frida frida-tools
```
## frida-il2cpp-bridge  
这个得去github上面看：
1. 创建文件结构 
2. npm install --save-dev frida-il2cpp-bridge
3. 编译 E:\frida-il2cpp-bridge-test\node_modules\.bin\frida-compile.cmd -o index.js .\index.ts -w
4. adb连接模拟器  adb connect 127.0.0.1:16385 adb端口号需要在设置里面查看
5. 获取手机root 权限 adb root
6. 查看模拟器cpu架构 getprop ro.product.cpu.abi  
结果是x86_64
7. 下载frida-server-17.2.15-android-x86_64 推送模拟器 adp push 
8. 获取权限 chmod 755 frida-server-17.2.15-android-x86_64 运行
9. frida-ps -U 查看正在运行进程  
frida-ps -Uai 列出安装的程序  
frida-ps -Ua 列出运行中的程序
10. adb shell pm list packages 列出所有安装的包
11. cat /proc/17042/maps 查看完整内存映射




