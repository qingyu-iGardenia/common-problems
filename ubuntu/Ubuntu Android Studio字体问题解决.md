# Ubuntu Android Studio字体问题解决

标签（空格分隔）： ubuntu android-studio

---

## 一、问题描述
> 在Ubuntu系统上安装Android Studio2.1 之后，发现软件的字体渲染有很大的问题，主要是字体发虚，相当的不好看。

## 二、解决过程
> 在发现这个问题之后，我Baidu了相当多的解决办法，都大同小异，最终也没有解决。但无意间却发现WebStorm的字体显示却是正常的。于是开始寻找它们之间的不同之处，最终发现WebStorm使用的是软件自带的一个jre。而Android Studio使用的则是系统的jre。于是将其拷贝过来，测试之，仍然没能解决问题。于是又仔细的看两个软件的启动脚本，发现Android Studio多配置了一个tools.jar，但是拷贝过来的这个jre文件夹中还没有这个tools.jar文件，于是又下载了idea，发现当中包含了tools.jar文件，果断将它的jre文件夹拷贝过来之。然后配置好这个tools.jar的路径。启动Android Studio，字体问题顺利的解决。

## 三、解决方案
> 下载idea，并将其中的jre文件夹拷贝到Android Studio目录下。


## 四、可能遇到的问题
> 1.在将jre文件夹拷贝完成之后，字体依然不正常，这时候需要打开设置，将软件的主题切换一下即可解决。
        

## 五、出现此问题可能的原因
> 1. 自己安装的JDK（OpenJdk/Oracle JDK）配置不正确
> 2. 自己安装的JDK缺少一些针对本系列软件特别的优化
    
## 六、其它可能可以解决该问题的方法
> 1. 使用一些ppa来安装JDK

