<div align="center">
  <a href="https://v2.nonebot.dev/store"><img src="https://github.com/A-kirami/nonebot-plugin-template/blob/resources/nbp_logo.png" width="180" height="180" alt="NoneBotPluginLogo"></a>
  <br>
  <p><img src="https://github.com/A-kirami/nonebot-plugin-template/blob/resources/NoneBotPlugin.svg" width="240" alt="NoneBotPluginText"></p>
</div>

<div align="center">

# nonebot-plugin-super-resolution

_✨ 动漫图像超分辨率增强 ✨_


<a href="./LICENSE">
    <img src="https://img.shields.io/github/license/A-kirami/nonebot-plugin-super-resolution.svg" alt="license">
</a>
<a href="https://pypi.python.org/pypi/nonebot-plugin-super-resolution">
    <img src="https://img.shields.io/pypi/v/nonebot-plugin-super-resolution.svg" alt="pypi">
</a>
<img src="https://img.shields.io/badge/python-3.8+-blue.svg" alt="python">

</div>

## 📖 介绍

通过超分辨率模型 [Real-CUGAN](https://github.com/bilibili/ailab/tree/main/Real-CUGAN) 来提高动漫图像质量

## 💿 安装

<details>
<summary>使用 nb-cli 安装</summary>
在 nonebot2 项目的根目录下打开命令行, 输入以下指令即可安装

    nb plugin install nonebot-plugin-super-resolution

</details>

<details>
<summary>使用包管理器安装</summary>
在 nonebot2 项目的插件目录下, 打开命令行, 根据你使用的包管理器, 输入相应的安装命令

<details>
<summary>pip</summary>

    pip install nonebot-plugin-super-resolution
</details>
<details>
<summary>pdm</summary>

    pdm add nonebot-plugin-super-resolution
</details>
<details>
<summary>poetry</summary>

    poetry add nonebot-plugin-super-resolution
</details>
<details>
<summary>conda</summary>

    conda install nonebot-plugin-super-resolution
</details>

打开 nonebot2 项目的 `bot.py` 文件, 在其中写入

    nonebot.load_plugin('nonebot_plugin_super_resolution')

</details>


## 🎉 使用
### 指令表
| 指令 | 需要@ | 范围 | 说明 |
|:-----:|:----:|:----:|:----:|
| 超分/放大/清晰 + 超分倍率 + 降噪配置 + 图片 | 否 | 群聊/私聊 | 超分发送的图片, 支持回复图片<br>参数可选, 具体见[参数表](#参数表) |

使用示例：

    /超分 三倍 <图像>

**注意**

默认情况下, 您应该在指令前加上命令前缀, 通常是 /

### 参数表
| 参数名  | 默认值 | 说明 |
|:-----:|:----:|:----:|
| 超分倍率 | 2倍 | 决定输出图片的尺寸, 越大处理需要时间越长。支持2倍、3倍、4倍 |
| 降噪配置 | 强力降噪 | **强力降噪**: 又称**三倍降噪**,如果原片噪声多，压得烂，推荐使用<br>**无降噪**: 适合原图噪声不多，想提高分辨率/清晰度/做通用性的增强、修复处理<br>**保守**: 如果你担心丢失纹理，担心画风被改变，担心颜色被增强，总之就是各种担心AI会留下浓重的处理痕迹，推荐使用 |