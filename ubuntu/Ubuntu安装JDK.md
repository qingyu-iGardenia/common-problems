# Ubuntu安装JDK

- 下载JDK安装文件到本地
- 创建一个文件夹来放置JDK
```shell
sudo mkdir -p /opt/java/jdk
```
- 将下载的JDK包解压到指定的目录下
```shell
sudo tar zvxf jdk-8u101-linux-x64.tar.gz -C /opt/java/jdk
```
- 设置环境变量
编辑/etc/profile文件，在末尾添加：
```shell
export JAVA_HOME=/opt/java/jdk/jdk1.8.0_101
export PATH=$JAVA_HOME/bin:$PATH
```
- 验证是否配置成功
```shell
java -version
javac
```
Tags： Ubuntu
