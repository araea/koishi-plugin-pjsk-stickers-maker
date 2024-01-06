# koishi-plugin-pjsk-stickers-maker

[![npm](https://img.shields.io/npm/v/koishi-plugin-pjsk-stickers-maker?style=flat-square)](https://www.npmjs.com/package/koishi-plugin-pjsk-stickers-maker)

## 🎈 介绍

这是一个基于 [Koishi](https://koishi.chat/) 框架的插件，可以让你使用 [Project SEKAI COLORFUL STAGE!](https://pjsekai.sega.jp/) 中的角色表情包来生成有趣的图片。🌈

你可以自定义表情包的 ID、文本内容、位置、旋转角度、字体大小和曲线效果，来创造出各种有趣的场景和对话。😂

你还可以查看所有可用的表情包列表，以及每个表情包的默认文本和样式。😍

## 📦 安装

```
前往 Koishi 插件市场添加该插件即可
```

## ⚙️ 配置

- `isSendEmojiIdWhenUndefined`：是否在未指定表情包ID时发送表情包ID信息，默认为 false。
- `isSendSpecificContent`：是否在未定义表情包ID时发送详细的参数教学信息，默认为 false。

## 🎮 使用

- 启动 `canvas` 服务：`koishi-plugin-canvas`（必须用这个喔）。
- 在 `Koishi` 默认根目录下，安装 `./data/pjsk/fonts` 文件夹内的两个字体。
- 启动插件，使用 `pjsk.drawList` 指令生成表情包 ID 列表。
- 建议为指令添加合适的别名。
- 如果想要添加额外的表情包，将图像文件（.png/.jpg/.gif）直接放入 `./data/pjsk/extraImg` 文件夹内即可。
- [上学大人的1700+米游社表情包资源下载](https://wwsy.lanzouj.com/ifgjH1jkeoyd)。

## 📝 命令

- `pjsk`：查看这个插件的帮助信息，了解如何使用它。

- `pjsk.draw -n [number:number] -y [positionY:number] -x [positionX:number] -r [rotate:number] -s [fontSize:number] -c [curve:boolean] -w [weight:number] --height [height:number] --color [color:string] [inputText:text]`：生成表情包图片，你需要指定一个文本参数，以及一些可选的选项参数（请将选项放在文本参数前面）。
  - `number` 是你想要使用的表情包的 ID，你可以使用 `pjsk.drawList` 命令来查看所有可用的表情包 ID，默认值是 -1，即随机。
  - `positionY` 是文本的垂直位置，可以是正数或负数，越大越靠下，默认值是 0。
  - `positionX` 是文本的水平位置，可以是正数或负数，越大越靠右，默认值是 0。
  - `rotate` 是文本的旋转角度，可以是正数或负数，越大越顺时针旋转，默认值是 0。
  - `fontSize` 是文本字体的大小，可以是正数或负数，越大字体越大，默认值是 0。
  - `curve` 是是否启用文本曲线效果，可以是 true 或 false，默认值是 false。
  - `weight` 是画布尺寸的宽度，可以是正数或负数，越大字体越大，默认值是 296。
  - `height` 是画布尺寸的高度，可以是正数或负数，越大字体越大，默认值是 256。
  - `color` 是文本字体的颜色，是颜色字符串，例如"#F09A04"，默认值是 ''。
  - `inputText` 是你想要显示在表情包上的文本内容，你可以使用斜杠（/）来换行。
  - 例如，你可以输入这样的命令：

```bash
pjsk.draw -n 1 -y 10 -x -10 -r 5 -s 2 -c -w 296 --height 256 --color #ff4757 你好/世界
```

- `pjsk.drawExtra`：同上。

- `pjsk.drawList`：查看所有可用的表情包列表，以及每个表情包的ID。

- `pjsk.drawListExtra`：同上。


## 🙏 致谢

感谢以下项目和资源的支持和帮助：

- [上学大人](https://www.npmjs.com/~shangxue) - 一个严肃的 ...？(e)
- [Koishi](https://koishi.chat/) - 一个灵活且强大的机器人框架
- [st.ayaka.one](https://st.ayaka.one/) - 一个提供 Project SEKAI 表情包的网站
- [Project SEKAI COLORFUL STAGE!](https://pjsekai.sega.jp/) - 一个充满魅力的音乐游戏
- [yunkuangao](https://github.com/yunkuangao) - `pjsk` 文件移动指导 修复若干 bugs ...（谢谢云哥喵 ~）
- [sekai-stickers](https://github.com/TheOriginalAyaka/sekai-stickers) - 一个提供 Project SEKAI 表情包的仓库

## 📄 License

MIT License © 2023
