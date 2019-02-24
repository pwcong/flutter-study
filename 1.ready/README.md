# 准备

## 1.学习dart语言

dart官网地址在这里：[https://www.dartlang.org](https://www.dartlang.org)

> 学习一门语言最好是通过敲栗子进行，而flutter使用dart语言进行开发，因此直接进行第二步，第一步作为语法参考文档

## 2.配置flutter开发环境

flutter官网地址在这里：[https://flutter.dev/](https://flutter.dev/)

配置步骤也很简单，步骤如下：

1. 直接下载[flutter安装包](https://flutter.dev/docs/get-started/install)安装，安装过程中涵盖dart语言库的安装因此无需独立去下载dart包安装。

2. 命令行输入`flutter doctor` 检查flutter当前开发环境状态，校验不通过的点可根据提示完成校验。其中必须通过的点如下：
  * 下载安装flutter（第一步的时候已完成）
  * 下载安装Android Studio，安装完成后打开然后下载adnroid的sdk
  * 连接手机开启调试模式或者启动手机模拟器如simulator或emulator

以下为验证通过后控制台输出的内容：

```sh
Doctor summary (to see all details, run flutter doctor -v):
[✓] Flutter (Channel stable, v1.0.0, on Mac OS X 10.13.6 17G5019, locale en-CN)
[✓] Android toolchain - develop for Android devices (Android SDK 28.0.3)
[✓] iOS toolchain - develop for iOS devices (Xcode 10.1)
[✓] Android Studio (version 3.2)
[✓] VS Code (version 1.31.1)
[✓] Connected device (1 available)

• No issues found!
```

## 3.其他

由于不可抗因素（dart与flutter是g家的东西），因此存在下载依赖包极度缓慢或者根本下载不了的情况，因此需要配置使用国内的mirror，这里介绍unix系统的配置信息，编辑`.bash_profile`文件，新增内容如下：
```
export PUB_HOSTED_URL=https://pub.flutter-io.cn
export FLUTTER_STORAGE_BASE_URL=https://storage.flutter-io.cn
```

然后执行以下命令：
```
flutter doctor
```

windows系统参照上述配置信息配置系统环境变量。