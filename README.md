# LinuxWeChatOCR

这是一个linux平台采用Python调用微信OCR功能，进行批处理图片OCR的代码, 基于 blueveryday 的 WeChatOCR 项目改造而来。

首先非常感谢blueveryday, swigger 以及其他对此做出贡献的朋友

原项目功能：

1. 将WeChatOCR.exe做了本地化，不再依赖微信的安装路径。
2. 将图片处理的格式多样化，增加了jpg，jpeg，bmp，tif格式的处理，只需要将文件放入scr文件夹中的即可。
3. 将OCR的处理结果将以docx格式保存到docx文件夹中。

本项目基于原项目 https://github.com/blueveryday/WeChatOCR ，改动如下：

1. 替换 ocr 原 win 依赖为 linux 依赖，作者测试 debian12 平台完全支持。
2. debian11 系统默认 Python 3.9.2，debian12 系统默认 Python 3.11.2。
3. 功能与原作者项目保持高度一致。

问题1:

```shell
root@shiny-intention:~/tgMonitor# python3 ocr.py 
Traceback (most recent call last):
  File "/root/tgMonitor/ocr.py", line 10, in <module>
    import wcocr
ImportError: libpython3.11.so.1.0: cannot open shared object file: No such file or directory
```

解决办法：

```shell
sudo apt update
sudo apt install python3.11 python3.11-dev

...

root@shiny-intention:~/tgMonitor# find /usr/lib /usr/local/lib -name "libpython3.11.so.1.0"
显示 /usr/lib/x86_64-linux-gnu/libpython3.11.so.1.0 为成功
```

