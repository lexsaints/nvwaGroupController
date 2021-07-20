## 介绍
女娲群控系统，免root控制安卓手机，安卓4.4版本以上的全部兼容

![Jietu20200126-152902.jpg](https://i.loli.net/2020/01/26/Jvl7jyp9OuILgaX.jpg)
![Jietu20200126-152948.jpg](https://i.loli.net/2020/01/26/c7lvKAwhTByELI2.jpg)


## 使用方法
1. 下载代码
`git clone https://github.com/zhongxia245/weiqunkong.git`
or
下载zip代码包,解压出来
2. 进入主目录下
3. 安装依赖`pip install -r requirements.txt`
5. 进入web文件夹,删除node_modules目录
6. 在web目录下：执行`npm install`
7. 在web目录下：执行`npm run serve`(需要先安装nodejs)
8. 浏览器打开`http://127.0.0.1:8000`
9. 手机连接到电脑，打开开发者模式，并信任电脑(电脑要安装adb)
  * 执行`adb push Main.dex /sdcard/Main.dex`
  * 执行`adb shell`
  * 执行命令 `export CLASSPATH=/sdcard/Main.dex`
  * 执行命令 `exec app_process /sdcard com.wanjian.puppet.Main &`
  * 执行`exit`，然后`adb forward tcp:8888 localabstract:puppet-ver1`
