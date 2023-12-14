# MistV2简明使用教程

本教程面向MistV2的非开发者用户，包括画手和其他使用MistV2对图片添加水印的个人。开发者用户请访问我们的项目代码仓库并按照代码仓库README文件提供的教程运行。本教程所使用的示例图片均已经过原画师授权。

## 目录

[安装](##安装)

[使用](##使用)

[常见问题](##常见问题)

## 安装

**步骤一**：从百度网盘或谷歌网盘安装Mist_v2

百度网盘：[https://pan.baidu.com/s/1fZP4nFxlmmr0DiE54DJ7HQ](https://pan.baidu.com/s/1fZP4nFxlmmr0DiE54DJ7HQ)（提取码：m4nx）

谷歌网盘：[https://drive.google.com/drive/folders/1vg8oK2BUOla5adaJcFYx5QMq0-MoP8kk](https://drive.google.com/drive/folders/1vg8oK2BUOla5adaJcFYx5QMq0-MoP8kk)

从百度网盘下载：

安装完百度网盘客户端后，点击上面的百度网盘链接，进入以下界面：

![img/P1.png](source/media/installation/P1.png)

之后单击`Mist_v2`文件夹，之后点击“下载”按钮：

![img/P2.png](source/media/installation/P2.png)

之后在弹出的客户端界面，指定下载路径之后，点击“下载”即可：

![img/P3.png](source/media/installation/P3.png)

![img/P4.png](source/media/installation/P4.png)

等待下载完成之后，在下载路径就会出现`Mist_v2`文件夹：

![img/P5.png](source/media/installation/P5.png)

![img/P6.png](source/media/installation/P6.png)

`Mist_v2`的文件结构如下：

- diffusers：水印的靶点模型（为开源版本的Stable Diffusion v1.5）
- Mist_GUI：Mist启动器对应的压缩包

`diffusers`文件夹里的内容（将会被用于**步骤九**）：

![img/P7.png](source/media/installation/P7.png)

`Mist_GUI`文件夹里的内容：

![img/P8.png](source/media/installation/P8.png)

之后，在`Mist_GUI`文件夹里面任选`Mist_GUI.rar`或`Mist_GUI.zip`其中一个压缩包进行解压缩即可，然后你可以把这个启动器放在任何一个你喜欢的位置（尽量放在除C盘以外的路径），这里使用的路径为`E:\Mist_GUI`：

![img/P9.png](source/media/installation/P9.png)

![img/P9.png](source/media/installation/P10.png)

其中的`Mist_GUI.exe`就是Mist启动器，单击即可运行。

从谷歌网盘下载：

点击上面的谷歌网盘链接，进入以下界面：

![img/P11.png](source/media/installation/P11.png)

将其中的所有文件全部下载即可，使用方法和百度网盘下载的版本同理。

**步骤二**：由于某些电脑运行`python`后会跳转到Microsoft应用商店，因此需要事先清除计算机中关于Microsoft应用商店的环境变量

点击开始菜单，并在搜索栏搜索并单击“编辑系统环境变量”

![img/P12.png](source/media/installation/P12.png)

单击后出现以下界面，然后点击“环境变量”：

![img/P13.png](source/media/installation/P13.png)

进入到这个界面，然后双击上方界面的"Path"这一栏：

![img/P14.png](source/media/installation/P14.png)

![img/P15.png](source/media/installation/P15.png)

然后如果列表中含有以`Microsoft\WindowsApps`结尾的这一项，先单击选中这一项，然后点击“删除”按钮进行删除：

![img/P16.png](source/media/installation/P16.png)

之后点击“确定”按钮使得修改生效：

![img/P17.png](source/media/installation/P17.png)

**必要时可以重启电脑使得环境配置生效。**

（或者可以参考该解决方案链接：[https://blog.csdn.net/qq_42365887/article/details/132486389](https://blog.csdn.net/qq_42365887/article/details/132486389)）

**步骤三**：安装启动器运行所需的动态库

该程序采用`.NET 7.0`编写，因此需要下载和`.NET 7.0`相关的动态库.

在整合包中已经包含了启动器运行所需的动态库，在`runtime`文件夹内：

![img/P18.png](source/media/installation/P18.png)

双击`windowsdesktop-runtime-7.0.13-win-x64.exe`进行安装即可：

![img/P19.png](source/media/installation/P19.png)

![img/P20.png](source/media/installation/P20.png)

出现以下信息说明安装成功：

![img/P21.png](source/media/installation/P21.png)

另外地，也可以通过点击以下链接下载所需的动态库：[https://dotnet.microsoft.com/zh-cn/download/dotnet/thank-you/runtime-desktop-7.0.13-windows-x64-installer](https://dotnet.microsoft.com/zh-cn/download/dotnet/thank-you/runtime-desktop-7.0.13-windows-x64-installer)

![img/P22.png](source/media/installation/P22.png)

**步骤四**：运行启动器

双击项目里的`Mist_GUI.exe`：

![img/P23.png](source/media/installation/P23.png)

然后会弹出以下界面：

![img/P24.png](source/media/installation/P24.png)

如果没有正常弹出界面，请检查**步骤三**有没有出现问题。

**步骤五**：通过启动器安装3.10.11版本的python

先去卸载电脑里原有的python（如果有的话）：

点击开始菜单，并在搜索栏搜索并单击“添加或删除应用程序”：

![img/P25.png](source/media/installation/P25.png)

然后在“应用列表”里面搜索“python”：

![img/P26.png](source/media/installation/P26.png)

之后点击右面的三个点，然后点击“卸载”：

![img/P27.png](source/media/installation/P27.png)

然后会卸载当前电脑上已经安装的python：

![img/P28.png](source/media/installation/P28.png)

出现以下信息说明卸载成功，点击“Close”按钮退出即可：

![img/P29.png](source/media/installation/P29.png)

然后点击启动器的`Install Python 3.10.11`按钮，会自动弹出python的安装页面：

![img/P30.png](source/media/installation/P30.png)

![img/P31.png](source/media/installation/P31.png)

记得勾选`Add Python 3.10 to PATH`，之后点击`Install Now`安装即可：

![img/P32.png](source/media/installation/P32.png)

出现以下信息说明安装成功，点击“Close”按钮关闭即可：

![img/P33.png](source/media/installation/P33.png)

**安装之后记得重启电脑，使得环境变量配置生效。**

**步骤六**：通过启动器安装Git

在启动器点击`Install Git`按钮安装Git：

![img/P34.png](source/media/installation/P34.png)

Git的安装均按照默认配置，一直点击“Next”按钮即可。

![img/P35.png](source/media/installation/P35.png)

![img/P36.png](source/media/installation/P36.png)

出现以下信息说明Git安装成功，点击“Finish”按钮即可：

![img/P37.png](source/media/installation/P37.png)

**步骤七**：如果是中国用户，则可以选择对pip切换安装源，使得下载依赖包的速度更快

如果要选择切换安装源，点击`Change Source`按钮即可：

![img/P38.png](source/media/installation/P38.png)

如果要换回默认的源，点击`Reset Source`按钮即可：

![img/P39.png](source/media/installation/P39.png)

**步骤八**：准备启动器的环境配置

**（注：运行这一步之前确保先给C盘清理出足够多（大约5GB以上）的空间，目的是给要下载的依赖包腾出空间。**

点击`Prepare Environment`按钮，即可进行启动器的环境配置。

![img/P40.png](source/media/installation/P40.png)

然后会弹出如下所示的命令行，表明进行启动器环境的安装：

![img/P41.png](source/media/installation/P41.png)

环境配置需要等待一段时间，待命令行自动关闭之后，环境配置完成。

如果要进行环境测试，点击`Test Environment`按钮即可。

![img/P42.png](source/media/installation/P42.png)

如果出现`Cuda is available: True`的情况，说明该机器是Nvidia系列显卡，并且可以使用gpu模式运行。

![img/P43.png](source/media/installation/P43.png)

如果出现`Cuda is available: False`的情况，说明该机器不可使用gpu模式运行，只能使用cpu模式运行。

如果点击`Test Environment`按钮时出现如下所示的错误信息：

![img/P44.png](source/media/installation/P44.png)

说明环境配置过程中出现了问题（例如命令行窗口中途突然关闭，突然断网，C盘剩余空间不够等等），建议点击`Clear Environment`按钮清除已经配好的环境，然后再点击`Prepare Environment`按钮进行配置即可。

![img/P45.png](source/media/installation/P45.png)

**步骤九**：放置水印的靶点模型

进入到项目的`mist-v2`文件夹：

![img/P46.png](source/media/installation/P46.png)

然后再进入`src`文件夹：

![img/P47.png](source/media/installation/P47.png)

之后我们关注其中的三个文件夹：

![img/P48.png](source/media/installation/P48.png)

这三个文件夹的作用分别为：

- `data`：便于存放要打上水印的图片和对比数据
- `output`：用于输出打过水印的图片
- `stable-diffusion`：用于存放水印的靶点模型

先进入到`data`文件夹：

![img/P49.png](source/media/installation/P49.png)

为了便于后续的使用，在`data`文件夹下面新建两个文件夹`contrast`和`img`：

![img/P50.png](source/media/installation/P50.png)

然后进入到`stable-diffusion`文件夹：

![img/P51.png](source/media/installation/P51.png)

将**步骤一**中`diffusers`文件夹下的`stable-diffusion-1-5`复制到启动器的`stable-diffusion`文件夹中：

![img/P52.png](source/media/installation/P52.png)

![img/P53.png](source/media/installation/P53.png)

这样放置水印的靶点模型步骤已经完成。

## 使用

### 界面

Mist WebUI的使用界面如下图所示：

![img/P54.png](source/media/installation/P54.png)

![img/P55.png](source/media/installation/P55.png)

**（重要）如何选择一次运行Mist添加水印的图片**：选择画风、内容具有一致性的5-10张图片一同添加水印为宜，一次添加水印的总图片数切忌超过15张。

**（重要）MistV2 GPU版本运行要求**：30系及之后发布的Nvidia显卡，显存6G以上

**（重要）MistV2 GPU版本运行时间**：默认参数处理5张图时间约为15分钟；运行时间大致和图片数量成正比

### 参数

WebUI含有两部分参数：常用参数和专业参数。前者为使用MistV2必须填写的参数，后者则对控制MistV2性能的起不同的作用。下面分表介绍两组参数。

**常用参数**：

| 参数名                  | 说明                                                                               | 如何填写                                                | 参数名                  |
| -------------------------- | ------------------------------------------------------------------------------------ | ----------------------------------------------------------- | -------------------------- |
| Strength（强度）       | 噪声的强度，越大保护效果越好。                                        | 换不同强度看看噪声效果，选择自己能接受的最大强度 | Strength（强度）       |
| Device（设备）         | 运行Mist的计算设备。GPU运行速度显著快于CPU。不懂显卡显存可以通过百度查显卡名字查到。 | 有6G显存以上显卡选GPU，其他情况选CPU          | Device（设备）         |
| Resizing（尺寸）       | 是否输出和原图相同尺寸的加噪图                                        | 保留默认值即可                                       | Resizing（尺寸）       |
| Mode（模式）           | 加水印的方法。Mode1针对色彩画，Mode3针对白描或二次元。Mode2加强了图生图防御。 | 二次元图选Mode3，其他选Mode1，特别在意防图生图效果可选Mode2 | Mode（模式）           |
| Data Path（数据路径） | 计算机上存放待加水印图片的位置                                        | 待加噪图片所在的路径                              | Data Path（数据路径） |
| Output Path（输出路径） | 输出水印图的位置                                                             | 找个空的文件夹即可                                 | Output Path（输出路径） |
| Model Path（模型路径） | 从我们提供的地址中下载模型压缩包并且直接解压到一个空的文件夹，即为该文件夹的地址 | 按说明填写                                             | Model Path（模型路径） |
| Class Path（对比数据路径） | 存放对比数据的位置                                                          | 使用一个空的文件夹即可                           | Class Path（对比数据路径） |
| Prompt（提示词）      | 概括待加水印图片的提示词                                                 | 概括图片的风格、内容，用逗号分割不同的短句 | Prompt（提示词）      |

**专业参数**：

| 参数名                                                    | 说明                                                                                               | 如何填写                                             |
| ------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------- | -------------------------------------------------------- |
| Class Prompt（对比数据提示词）                      | 用于生成对比数据的提示词                                                                 | 保持和提示词一致即可                           |
| Training epochs of Mist-V2（攻击训练步数）           | 总攻击轮数；越大的轮数对多步LoRA的针对性越强，但也越容易跑偏，同时图生图效果会减弱 | 非研究用途保持默认值即可                     |
| Training steps of LoRA in one epoch（单轮LoRA训练步数） | 一轮攻击中目标模型的训练步数；越多的步数对多步LoRA的针对性越强，但也越容易跑偏，同时图生图效果会减弱 | 非研究用途保持默认值即可                     |
| Training steps of attacking in one epoch（单轮攻击训练步数） | 一轮攻击中攻击的训练步数；越多步数攻击效果越好，但运行时间也会相应增加 | 可以调大到自己可接受的最大值               |
| The learning rate of LoRA                                    | 靶点LoRA学习率                                                                                  | 非研究用途保持默认值即可；也可尝试调到LoRA训练最常用的值 |
| The learning rate of PGD（攻击步长）                   | 攻击学习率                                                                                      | 非研究用途保持默认值即可                     |
| The weight of prior loss（对比数据影响因子）       | 对比数据在攻击中的影响                                                                    | 非研究用途保持默认值即可                     |
| The weight of vae loss（Mode 2影响因子）               | 仅在启动Mode 2后有效，因子越大，防图生图效果越强，相应的其他性能会有一定损失 | 按个人需求调整，不要改变因子的数量级   |
| LoRA Ranks                                                   | 靶点LoRA阶数                                                                                     | 非研究用途保持默认值即可；也可尝试调到LoRA训练最常用的值 |

### 使用实例

完成环境配置之后，在启动器中点击`Run Mist`即可运行Mist Webui。

![img/P56.png](source/media/installation/P56.png)

![img/P57.png](source/media/installation/P57.png)

查看Mist WebUI的方式是：使用任意一个浏览器，在地址栏输入`http://127.0.0.1:7860`即可。

![img/P58.png](source/media/installation/P58.png)

将要等待打水印的图片放在`mist-v2/src/data/img`文件夹：（示例图已经过原画师授权）

![img/P59.png](source/media/installation/P59.png)

![img/P60.png](source/media/installation/P60.png)

![img/P61.png](source/media/installation/P61.png)

![img/P62.png](source/media/installation/P60.png)

![img/P63.png](source/media/installation/P63.png)

然后在Webui中按照以下的参数填写：

| 参数 | 值 |
| :-: | :-: |
| Data Path | data/training |
| Output Path | output |
| Target Model Path | stable-diffusion/stable-diffusion-1-5 |
| Path to place contrast images | data/contrast |
| Prompt | （按照个人喜好或实际情况填写即可，这里的例子为masterpiece, best quality） |

![img/P64.png](source/media/installation/P64.png)

填写完毕后，点击Webui内的`Mist`这个按钮开始运行：

![img/P65.png](source/media/installation/P65.png)

命令行内出现类似以下内容说明已经成功处于运行中：

![img/P66.png](source/media/installation/P66.png)

在运行结束后，被打上水印的图片将被放在`output`文件夹：

![img/P67.png](source/media/installation/P67.png)

![img/P68.png](source/media/installation/P68.png)

可以点击图片查看效果：

![img/P69.png](source/media/installation/P69.png)

## 常见问题

Q: 点击`Prepare Environment`按钮运行不了，并遇到打开Microsoft应用商店的情况怎么办？

A: 解决方法参见步骤二。（或者可以参考该解决方案链接：[https://blog.csdn.net/qq_42365887/article/details/132486389](https://blog.csdn.net/qq_42365887/article/details/132486389)）

Q: 程序运行时出现以下报错信息，是否会影响使用？

```txt
A matching Triton is not available, some optimizations will not be enabled.
Error caught was: No module named 'triton'
```

A: 这个是由于`xformers`库安装在Windows环境下导致的，直接忽略即可，不会影响Mist的使用。

Q: 如果配置环境过程中出现`No space left on device`怎么办？

A: 这个是由于C盘剩余空间太小导致的，给C盘清理出足够多（大约5GB以上）的空间即可。

Q: 如果点击完`Install Python 3.10.11`按钮再点击`Prepare Environment`按钮出现`Couldn't launch python`错误怎么办？

![img/P70.png](source/media/installation/P70.png)

A: 这是安装完python之后环境变量没有更新导致的，重启电脑再运行启动器即可。
