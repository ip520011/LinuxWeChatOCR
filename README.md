# LinuxWeChatOCR

这是一个linux平台采用Python调用微信OCR功能，进行批处理图片OCR的代码, 基于 blueveryday 的 WeChatOCR 项目改造而来。

首先非常感谢blueveryday, swigger 以及其他对此做出贡献的朋友

原项目功能：

1. 将WeChatOCR.exe做了本地化，不再依赖微信的安装路径。
2. 将图片处理的格式多样化，增加了jpg，jpeg，bmp，tif格式的处理，只需要将文件放入scr文件夹中的即可。
3. 将OCR的处理结果将以docx格式保存到docx文件夹中。

本项目基于原项目 https://github.com/blueveryday/WeChatOCR ，改动如下：

1. 根据linux替换ocr相关依赖。
2. 功能与原作者项目保持高度一致。

