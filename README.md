## CheatSheet Template

基于 [Milvoid/CheatingSheetTemplate](https://github.com/Milvoid/CheatingSheetTemplate) 修改的 A4 竖向四栏 Cheat Sheet 模板。

> [!IMPORTANT]
> 字体版权归属 Apple Inc.。根据其用户协议，您仅可在 Apple 平台上使用这些字体，而不应进行分发。

### 文件结构

```text
.
├── CheatSheet.tex          # 主文件
├── config/
│   ├── style.tex           # 页面、字体、颜色、排版样式
│   └── commands.tex        # 自定义命令与环境
├── fig/                    # 图片文件
└── fonts/                  # 字体文件
```

### 快速上手

该模板必须使用 **XeLaTeX** 编译，不能使用 pdfLaTeX 编译。

在项目根目录运行：

```sh
xelatex CheatSheet.tex
```

如需自动处理多次编译，可使用 `latexmk`：

```sh
latexmk -xelatex CheatSheet.tex
```

编译需求：

- 已安装 TeX Live、MacTeX 或其他包含 XeLaTeX 的 LaTeX 发行版。
- `fonts/` 目录存在，并包含 `SFCompactText-*.ttf` 与 `PingFangSC-*.ttf` 字体文件。字体必须放在此文件夹内。
- 编译命令在仓库根目录执行，否则相对路径 `config/`、`fig/`、`fonts/` 可能无法正确解析。

修改内容：

- 主要内容写在 `CheatSheet.tex` 的 `cheatsheet` 环境内。
- 页面尺寸、栏宽、栏距、字号、颜色等样式集中在 `config/style.tex`。
- 常用命令放在 `config/commands.tex`。

### Font

- 英文字体：SF Compact Text
- 中文字体：苹方 简

### Typography

- Section Title：7 pt
  - 中文、英文均为 Regular
- Subsection Title：6 pt
  - 中文、英文均为 SemiBold
- Paragraph / Bullet Point：5 pt
  - 中文、英文均为 SemiBlack
- 正文：5 pt
  - 中文、英文均为 Regular
- 行间距：6 pt

### Color

- Section Title：`#004D80`
- Subsection Title：`#004D80`
- Paragraph：`#0076BA`
- 正文：标准黑色

### Page

- 尺寸：标准竖向 A4
- 页边空白：左、右、上为 `0.10 cm`；底部为 `0.25 cm`
- 四栏布局：每个 Column 为 `5.07 cm`
- Column 间距：三个栏间距均为 `0.2 cm`

### Divider

- `0.5 pt` 水平分割线，长度与 column 一致
- 分割线上下各与文字保留 `1 pt` 空隙
- 颜色为 `#808080`