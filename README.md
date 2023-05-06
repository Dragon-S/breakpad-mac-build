# breakpad-mac-build

在Mac M1上编译arm64和x86_64版本

一、mac M1上编译arm64

1、获取depot_tools并设置PATH

git clone https://chromium.googlesource.com/chromium/tools/depot_tools.git

export PATH=$PATH:/Users/lorne/Develop/code/mac-code/breakpad/depot_tools

2、获取breakpad代码并编译

mkdir breakpad && cd breakpad

fetch breakpad

cd src

./configure --prefix=/Users/lorne/Develop/code/mac-code/breakpad/breakpad/src/out/arm64

make

make install



二、在Mac M1上编译x86_64

1、终端设置x86_64

打开terminal，输入下面命令

arch -x86_64 /bin/zsh

2、同Mac M1上编译arm64

三、附件

1、参考

https://chromium.googlesource.com/breakpad/breakpad

https://commondatastorage.googleapis.com/chrome-infra-docs/flat/depot_tools/docs/html/depot_tools_tutorial.html#_setting_up

2、注意事项

（1）每次configure前需要clean

make distclean
