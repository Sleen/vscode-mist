# Mist 插件

## 使用

大部分功能需要编辑器语言设置为 `MIST` 才能使用，如果是 `.mist` 文件，会自动设置为 `MIST` 语言。

## 代码高亮

对模版中表达式进行语法高亮。对模版中的错误进行提示，目前包括 Json 语法错误、重复属性、表达式语法。

<img src="https://raw.githubusercontent.com/Vizzle/vscode-mist/master/readme/highlight.jpg" width="414px"/>

## 代码提示

编写 Mist 模版时会根据上下文提示当前可用属性，鼠标移到属性名或枚举值上可以显示属性描述。

<video width="770px" controls style="border-radius:4px" autoplay loop>
  <source src="https://gw.alipayobjects.com/os/rmsportal/scfbArcHAZkpWhRSwIff.mp4" type="video/mp4">
Your browser does not support the video tag.
</video>

## 模版布局结构

在编辑 Mist 模版文件时，左侧的资源管理器里的 `MIST OUTLINE` 会显示模版的布局结构和 node 的一些关键信息，方便定位。点击节点可选中并跳转到对应的代码位置。

<img src="https://raw.githubusercontent.com/Vizzle/vscode-mist/master/readme/outline.jpg" width="372px"/>

## 注释

可以在模版中使用 `//` 和 `/* */` 添加注释，注释能被正常高亮、[格式化](#格式化)，并且在 `MIST OUTLINE` 中也会显示元素的注释。推荐在模版中多用注释，方便修改时快速定位元素。

## 格式化

在编辑器中右键选择 `Format Document` 可以格式化当前文档，也可使用快捷键 `⇧` `⌥` `F` 或自定义其它快捷键。

选中文本时右键选择 `Format Selection` 可格式化选中部分。

## 快速跳转

点击编辑器右上角的 <img src="https://raw.githubusercontent.com/Vizzle/vscode-mist/master/readme/show_data_icon.png" width="16px"/> `Show Data File` 按钮可以从模版文件跳转到对应的数据文件（.json），并滚动到引用该模版的位置。如果找到多个文件或位置使用该模版，会弹出选择框。

目前按照正则式匹配，并只在模版所在目录下查找 `.json` 文件，不一定能正确找到。

## 调试

点击编辑器右上角的 <img src="https://raw.githubusercontent.com/Vizzle/vscode-mist/master/readme/start_icon.png" width="14px"/> `Start Mist Debug Server` 按钮开启调试服务器。开启后图标会变成停止图标，点击可以关闭服务器。

目前有个小问题是，使用过这个功能后模版文件夹下会自动添加一个 `.vscode` 文件夹，里面保存了 `Mist` 插件的配置文件，可以把这个文件夹添加到 `.gitignore` 里。
