# flet-on-google-idx

Starter files to run a [Flet](https://flet.dev) application on the [Google IDX platform](https://idx.google.com/).

Feel free to fully adapt to your needs!

**VIDEO TUTORIAL: https://youtu.be/TiW-JTd4EP0**

**ARTICLE: https://ndonkohenri.medium.com/running-packaging-a-flet-app-on-google-idx-60680db6f487**


********************************************************************************************************************************
2025018
导入仓库Import Git Repo
https://github.com/nnyaa/flet-idx
选择This is a Flutter app

需要重新rebuild evenment

建立sdK目录
mkdir  ~/Android-sdk 


下载Android SDK 的命令行工具
wget   https://dl.google.com/android/repository/commandlinetools-linux-11076708_latest.zip
unzip   commandlinetools-linux-11076708_latest.zip


设置sdk路径，Android SDK 目录 <sdk>/cmdline-tools/latest/ 目录下
export ANDROID_SDK_ROOT=<sdk>           （不应再重新目录下）  ANDROID_SDK_ROOT="/home/user/android-sdk/sdk"
export PATH=$PATH:$ANDROID_SDK_ROOT/cmdline-tools/latest/bin  （latest必须，若无移动之）/home/user/android-sdk/sdk/cmdline-tools/latest/bin
长期使用：在你的 ~/.bashrc 或 ~/.bash_profile 文件中添加


进入venv测试并升级
source  .venv/bin/activate
sdkmanager --update

安装安卓SDK
sdkmanager --sdk_root=$ANDROID_SDK_ROOT --install "platform-tools" "platforms;android-30" "build-tools;30.0.3"
********************************************************************************************************************************************************
