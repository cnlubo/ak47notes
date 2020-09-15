
# windows 10

## scoop

### 安装

- 確保你允許PowerShell執行本地腳本

```bash
set-executionpolicy remotesigned -scope currentuser

```

- 指定安裝目錄

```bash

  $env:SCOOP='D:\Applications\Scoop'


[Environment]::SetEnvironmentVariable('SCOOP', $env:SCOOP, 'User')

iwr -useb get.scoop.sh | iex

```

- 增加bucket

```bash

scoop bucket add extras

scoop bucket known

```

- 设置代理

```bash
scoop config proxy 127.0.0.1:1080

```

- 常用软件安装

```bash
scoop install sudo;
scoop install aria2;

```

- 安装和切换不同的 Java (JDK)版本

```bash
# java
scoop bucket add java
# jdk 1.8
scoop install ojdkbuild8-full
java -version
# openjdk10
java -version

# 切换1.8
scoop reset ojdkbuild8-full
# 切换openjdk 10 
scoop reset openjdk10

```

- 安装和切换python

```bash
scoop bucket add versions

```

## 字体

### 更纱字体

更纱字体: <https://github.com/be5invis/Sarasa-Gothic/>

更纱黑体 UISC: 即 Sarasa UI SC (SC代表Simplified Chinese,简体中文.)

### Fira Code

github:<https://github.com/tonsky/FiraCode>

- 下载最新字体
- 解压缩下载文件，并进入ttf文件夹
- 选中所有字体文件，右键选择安装

## mactype

网址：<https://github.com/snowie2000/mactype>

### 字体安装工具 - noMeiryoUI

网址：noMeiryoUI

### 修改Chrome字体设置

将字体换为更纱黑体之后, 显示效果并不是很好，需要结合油猴插件质感字体&&页面平滑滚动增强字体的显示效果。
脚本安装地址：<http://suo.im/61ZO1o>

## vscode 配置 字体

- 打开vscode的配置页面，并搜索font
- 修改editor.fontFamily配置项的内容为：'Fira Code Retina', 'Sarasa Term SC Regular'。Fira Code为首选字体，更纱黑体为备选字体。
- 勾选editor.fontLigatures配置，启用连字符
- 配置字体过程中若提示字体无法识别，尝试配置后重启vscode，返回vscode编辑器，输入@，r，&字符验证字体是否生效。

## windows Terminal

github: <https://github.com/microsoft/terminal/releases>

安装: choco install microsoft-windows-terminal

## 自定义 Windows PowerShell 和 cmd 的字体

### 更换 PowerShell 的配色

```bash
scoop install colortool

```

# powershell 7 美化

```bash
# 字体
git clone https://github.com/powerline/fonts.git --depth=1
cd fonts
./install.ps1
# 安装完毕删除 fonts 文件夹即可

```
