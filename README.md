﻿# Starsector-096-Localization

本项目为《远行星号》游戏的中文翻译项目。

目前正在进行的是游戏 **0.96a** 版本的汉化，尚在启动阶段。

## 下载汉化

**注意：本汉化包仅适用于 0.96a-RC10 版本**

### 从论坛下载

目前0.96尚且没有打包的汉化包。您可以在论坛帖子 [远行星号 0.95.1a-RC6 中文汉化v1.0.0](https://www.fossic.org/thread-3060-1-1.html) 下载最新的汉化版游戏安装包。

### 下载 GitHub 上的最新汉化

如果您希望抢先体验汉化内容，请参照如下步骤下载汉化：

1. 下载汉化文件
   1. [点这里下载汉化文件](https://github.com/TruthOriginem/Starsector-096-Localization/archive/refs/heads/master.zip)
   2. 解压下载的文件，其中应包括名为`localization`的文件夹
2. 安装汉化文件
   1. 打开游戏目录下的`starsector-core`文件夹
   2. 将下载解压文件中`localization`文件夹内的全部内容复制到`starsector-core`文件夹中
      1. 如提示文件已存在，请选择【覆盖】
3. 正常游玩，**如果遇到翻译质量问题或bug，请向我们报告**。
   1. 由于汉化尚未完成，出现未翻译英文属于正常现象，无需报告。 

## 参与汉化

如果想参与汉化或者想为汉化提出意见和建议，请通过 QQ 553816216 添加 **议长**的好友，或者申请加入 QQ 群 **788249918 汉化顾问团**，然后才申请加入本项目。
申请入群时**请注明你的来历和英语水平**，英语水平需达到 **CET6** 或更高。

之后，参照这个[非常简单的翻译指南](docs/tut_translator.md)开始使用Paratranz平台进行翻译

## 译文格式规范

请参见[远行星号译文格式规范](docs/format_standard.md)

## 译名表

请参见[远行星号术语参考表](https://paratranz.cn/projects/3489/terms)

## 项目管理

### 文件夹结构

* "版本号 + data"是游戏各个版本原始的 data 文件夹
* "original" 内存放当前版本的英文原文，不要改动
* "original.old" 内存放上个版本(0.95.1a-RC6)的英文原文，不要改动
* "localization" 内存放当前版本的译文
* "localization.old" 内存放上个版本(0.95.1a-RC6)的译文
* "para_tranz" 内存放Paratranz平台相关脚本
* "docs" 内存放项目文档内容

### 自动化脚本

* **Python环境: 3.10 或更高**

| 文件                  | 作用                                                    |
|-----------------------|-------------------------------------------------------|
| _cleanLocalization.py | 根据original文件夹清理localization文件夹。                     |
| _copyOldLocalization.py | 通过比对original文件夹，更新汉化包中的未变更文件。                     |
| _handleVariantNames.py | 处理指定文件夹中所有装配名，并更新/使用映射 json 用于翻译。                     |
| _swapLangFile.py       | 用来更替汉化文件和英文文件的脚本。                                     |
| _variant_name_map.json | 装配名映射文件，英文名对应汉化名，可后继继续更新。                             |
| para_tranz.py         | 用于ParaTranz平台的数据导入导出工具，使用方法参见[本指南](docs/tut_admin.md) |

### 版本汉化流程

![][flow-chart]

[flow-chart]:docs/flow_chart.png
