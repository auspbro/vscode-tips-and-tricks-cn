
# [VS Code](https://code.visualstudio.com) 提升编码效率的技巧集

> 英文版请参考 [VS Code Tips and Tricks](https://github.com/auspbro/vscode-tips-and-tricks-cn/blob/master/README_EN.md)

> 文中内容提到的快捷键操作有可能和最新版本有所出入，最新版本的键盘快捷键请参考[这里](https://code.visualstudio.com/docs/getstarted/keybindings)

# 内容目录

1. <a href="#入门">入门</a>
2. <a href="#自定义">自定义</a>
3. <a href="#插件扩展">插件扩展</a>
4. <a href="#文件及文件夹管理">文件及文件夹管理</a>
5. <a href="#进阶编辑">进阶编辑</a>
6. <a href="#智能提示">智能提示</a>
7. <a href="#创建代码片段">创建代码片段</a>
8. <a href="#Git 集成">Git 集成</a>
9. <a href="#调试">调试</a>
10. <a href="#运行任务">运行任务</a>
11. <a href="#其他资源">其他资源</a>


# 入门

## VS Code 内部测试版本

Visual Studio Code 开发团队使用内测版用于测试 VS Code 最新功能及便于 bug 修复。内测版可以在[这里](https://code.visualstudio.com/insiders)下载。

* 对早期使用者而言 - 内测版的代码更新比较快可能会导致各种 bug。
* 频繁的版本更新 - 频繁更新开发版会修复最近的 bug 和提供新的功能尝鲜。
* 多版本共存安装 - 内测版和稳定版可以同步安装到系统并且独立使用互不影响。

![多版本共存安装](/media/side-by-side-install.png)

## 准备开始

打开**欢迎**页面进入 VS Code 大门。 **帮助** > **欢迎**。

![欢迎页面](/media/welcome_page.png)

欢迎页面有**交互式演练场**用于互动演示 VS Code 的一些功能

![interactive playground](/media/interactive_playground.png)

## 命令面板

命令面板可以基于当前输入的内容访问所有提供的命令入口

> Mac: <kbd>cmd+shift+p</kbd> or <kbd>f1</kbd>

> Windows / Linux: <kbd>ctrl+shift+p</kbd> or <kbd>f1</kbd>

![命令面板](/media/OpenCommandPalatte.gif)

## 组合键参考

在**命令面板**中的所有命令都有与之对应的快捷键（如果有的话）。如果你忘记快捷键是什么，可以打开**命令面板**来查看。

![keyboard references](/media/keyboard-references.png)

## 快捷开启

快速的打开文件和运行相关命令(操作如下)
> Mac: <kbd>cmd+p</kbd>

> Windows / Linux: <kbd>ctrl+p</kbd>

![Quick Open](/media/QuickOpen.gif)

> **提示:** 输入 "?" 查看帮助

### 在最近打开过的文件之间切换

重复按下**快捷开启**快捷键会重复在最近打开过的文件之间切换

### 使用快捷开启打开多个文件

你可以通过**快捷开启**方式按下键盘右键在后台打开当前项目的多个文件。

## CLI 工具

> Linux: 请参考[这里](https://code.visualstudio.com/docs/editor/setup#_linux)。

> Windows: 请参考[这里](https://code.visualstudio.com/docs/editor/setup#_windows)。

> Mac: 请参考以下

打开 **命令面板** (<kbd>F1</kbd>) 输入 "shell command". 敲回车执行 **Shell 指令: 安装 'code' 指令到环境变量**.

![shell 指令](/media/setup_shell-command.png)


```bash
# 在 VS Code 中打开当前目录 
code .

# 在最近使用过的 VS Code 窗口打开当前目录
code -r .

# 创建新的窗口
code -n

# 更改语言
code --locale=es

# 打开 diff 编辑器比较文件
code --diff <file1> <file2>

# 查看帮助选项
code --help

# 禁用所有扩展
code --disable-extensions .
```

![all cli commands](/media/vscode-cli-commands.png)

## .vscode 文件夹

工作区 `.vscode` 中的特殊文件。例如：Task Runner 的 `tasks.json` 和 debugger 的 `launch.json`。

## 状态栏

**错误和警告**

> Mac: <kbd>shift+cmd+m</kbd>

> Windows / Linux: <kbd>ctrl+shift+m</kbd>

快速跳转到项目出错和警告的位置,如果是 Markdown 文件按下 <kbd>ctrl+shift+m</kbd> 默认是把编辑器拆分成预览窗口。

重复切换定位错误 <kbd>f8</kbd> 或 <kbd>shift+f8</kbd>

![errors and warnings](/media/Errors_Warnings.gif)

你可以通过输入（'errors','warnings'）或匹配的文本来过滤筛选问题。

**更换语言模式**

> Mac: <kbd>cmd+k m</kbd>

> Windows / Linux: <kbd>ctrl+k m</kbd>

![change syntax](/media/change_syntax.gif)

如果你想给文件存留成新的语言模式，可以在编辑器右下角通过**选择语言模式...**命令来关联一个已经安装好的语言到当前文件。

# 自定义

·通过自定义 VS Code,你可以做更多事情

* 更换主题
* 更换键盘快捷键
* 调整设定
* 添加 Json 许可
* 创建代码片段
* 安装扩展

查看完整 [文档](https://code.visualstudio.com/docs/getstarted/settings).

## 更改主题

打开 **命令面板** 输入"themes". 你可以在扩展商店安装更多主题。

![Preview themes](/media/PreviewThemes.gif)

另外你可以安装更改文件图标的主题

![File icon themes](/media/PreviewFileIconThemes.gif)

## 更换键盘快捷键

### 键盘快捷键参考文档

对应的平台的快捷键参考文档 ([macOS](https://go.microsoft.com/fwlink/?linkid=832143), [Windows](https://go.microsoft.com/fwlink/?linkid=832145), [Linux](https://go.microsoft.com/fwlink/?linkid=832144)).

![Keyboard Reference Sheet](/media/KeyboardReferenceSheet.png)

### 键映射

如果你习惯于某种编辑器的快捷键，可以安装快捷键扩展到 VS Code 来导入你常用的编辑器的快捷键。 选择 **首选项** > **键映射扩展** 去 [扩展商店](https://marketplace.visualstudio.com/search?target=VSCode&category=Keymaps&sortBy=Downloads) 查看当前列表。 比较流行的一些键迎神插件如下:

- [Vim](https://marketplace.visualstudio.com/items?itemName=vscodevim.vim)
- [Sublime Text 键映射](https://marketplace.visualstudio.com/items?itemName=ms-vscode.sublime-keybindings)
- [Emacs 键映射](https://marketplace.visualstudio.com/items?itemName=hiro-sun.vscode-emacs)
- [Atom 键映射](https://marketplace.visualstudio.com/items?itemName=ms-vscode.atom-keybindings)

### 自定义键盘快捷键

打开 **命令面板** 输入"keyboard shortcuts" 现在可以在文件的右侧添加你自己的组合键了。

![customize keyboard shortcuts](/media/KeyboardShortcuts.gif)

查看更多关于 [Visual Studio Code](https://code.visualstudio.com/docs/getstarted/keybindings) 自定义快捷键内容。

## 自定义设置·

打开 `settings.json`

> Mac: <kbd>cmd+,</kbd>

> Windows / Linux: **文件** > **首选项** > **设置**

*Format on paste*

```json
"editor.formatOnPaste": true
```

*更改字体大小*

```json
"editor.fontSize": 18
```

*更改缩放等级*

```json
"window.zoomLevel": 5
```

*font ligatures*

```json
"editor.fontFamily": "Fira Code",
"editor.fontLigatures": true
```

> **提示:** 你需要安装一个支持 font ligatures 的字体。 [FiraCode](https://github.com/tonsky/FiraCode) is a popular font on the VS Code team.

![font ligatures](/media/font-ligatures-annotated.png)

*自动保存*

```json
"files.autoSave": "afterDelay"
```

你也可以在最高级菜单 **文件** > **自动保存** 开启自动保存。

*Format on save*

```json
"editor.formatOnSave": true,
```

*改变缩进的字符长度*

```json
"editor.tabSize": 4
```

*空格还是缩进*

```json
"editor.insertSpaces": true
```

*Render whitespace*

```json
"editor.renderWhitespace": "all"
```

*忽略文件或者文件夹*

从编辑器窗口移除这些文件或者文件夹

```json
"files.exclude": {
        "somefolder/": true,
        "somefile": true
}
```

从搜索结果中移除这些文件或者文件夹。

```json
"search.exclude": {
    "someFolder/": true,
    "somefile": true
}
```

还有许多[其他的功能](https://code.visualstudio.com/docs/getstarted/settings)。

## 特定的语言设置

你可以只为某些特定的语言设置

```json
"[languageid]": {

}
```

> **提示:** 你可以在 **命令面板** 输入 "Configure language specific settings" 找到 language id

![language based settings](/media/lang-based-settings.png)

## 添加 JSON 认可

多数文件默认是启用的，在 `settings.json` 创建你自己的 schema 和 validation。

```json
"json.schemas": [
    {
        "fileMatch": [
            "/bower.json"
        ],
        "url": "http://json.schemastore.org/bower"
    }
]
```

或者在你的工作区定义一个 schema

```json
"json.schemas": [
    {
        "fileMatch": [
            "/foo.json"
        ],
        "url": "./myschema.json"
    }
]
```

或者自定义一个 schema

```json
"json.schemas": [
    {
        "fileMatch": [
            "/.myconfig"
        ],
        "schema": {
            "type": "object",
            "properties": {
                "name" : {
                    "type": "string",
                    "description": "The name of the entry"
                }
            }
        }
    },
```

查看更多 [文档](https://code.visualstudio.com/docs/languages/json).

# 插件扩展

## 查找扩展

1. 在 VS Code [商店](https://marketplace.visualstudio.com/vscode).
2. 在 VS Code 内搜索
3. 查看推荐的扩展
4. 社区创建的扩张列表，例如 [awesome-vscode](https://github.com/viatsko/awesome-vscode).

## 安装扩展

点击编辑器左侧活动栏的扩展按钮，然后你可以通过搜索窗口或者点击**更多** (...) 按钮来选择过滤和通过安装计数的排序方式安装想要的扩展。

![install extensions](/media/InstallExtensions.gif)

## 扩展推荐

点击活动栏的扩展按钮，然后点击**更多** (...) 按钮菜单选中**显示推荐的扩展**即可

![show recommended extensions](/media/ShowRecommendedExtensions.gif)

## 创建自己扩展

如果你对创建自己的扩展感兴趣，可以看看这个[文档](https://code.visualstudio.com/docs/extensionAPI/extension-points)。

* configuration
* commands
* keybindings
* languages
* debuggers
* grammars
* themes
* snippets
* jsonValidation

# 文件及文件夹管理

## 集成终端

> Windows / Linux / Mac: <kbd>ctrl+`</kbd>

![Integrated terminal](/media/integrated_terminal.png)

进一步了解：

- [官方文档](https://code.visualstudio.com/docs/editor/integrated-terminal)
- [精通 VS Code 终端的文章](http://www.growingwiththeweb.com/2017/03/mastering-vscodes-terminal.html)


## 自动保存

使用 <kbd>cmd+,</kbd> 打开 `settings.json` 

```json
"files.autoSave": "afterDelay"
```

你也可以在顶层菜单栏通过 **文件** > **自动保存** 来触发自动保存功能。

## 切换侧边栏

> Mac: <kbd>cmd+b</kbd>

> Windows / Linux: <kbd>ctrl+b</kbd>

![toggle side bar](/media/toggle_side_bar.gif)

## 免打扰模式

> Mac: <kbd>cmd+k z</kbd>

> Windows / Linux: <kbd>ctrl+k z</kbd>

![zen mode](/media/zen_mode.gif)

开启免打扰模式。


## 拆分编辑器

> Mac: <kbd>cmd+\\</kbd> 或者 <kbd>cmd</kbd> 然后从文件管理器点击一个文件

> Windows / Linux: <kbd>ctrl+\\</kbd>

> Linux: <kbd>ctrl+2</kbd>

![split editors](/media/split_editor.gif)

你可以使用拖拽的方式来创建新的编辑器组以及在编辑器组之间移动

## 在编辑器标签页之间切换

> Mac: <kbd>cmd+1</kbd>, <kbd>cmd+2</kbd>, <kbd>cmd+3</kbd>

> Windows / Linux: <kbd>ctrl+1</kbd>, <kbd>ctrl+2</kbd>, <kbd>ctrl+3</kbd>

![navigate editors](/media/navigate_editors.gif)

## 切换到资源管理窗口

> Mac: <kbd>cmd+shift+e</kbd>

> Windows / Linux: <kbd>ctrl+shift+e</kbd>

## 创建并打开一个文件

> Mac: <kbd>cmd+click</kbd>

> Windows / Linux: <kbd>ctrl+click</kbd>

![create and open file](/media/create_open_file.gif)

## 关闭当前打开的标签页。

> Mac: <kbd>cmd+w</kbd>

> Windows / Linux: <kbd>ctrl+k f</kbd>

## 回溯操作历史

回溯上一个编辑过的文件 <kbd>ctrl+tab</kbd>


回溯历史操作。

> Mac: <kbd>ctrl+-</kbd>

> Windows / Linux: <kbd>alt+left</kbd>

向前回溯历史操作。

> Mac: <kbd>ctrl+shift+-</kbd>

> Windows / Linux: <kbd>alt+right</kbd>

![navigate history](/media/navigate_history.gif)

## 回顾并切换到历史的某个文件

> Mac: <kbd>cmd+e</kbd> 或 <kbd>cmd+p</kbd>

> Windows / Linux: <kbd>ctrl+e</kbd> 或 <kbd>ctrl+p</kbd>

![navigate to file](/media/navigate_to_file.gif)

## 文件关联

为一些无法准确识别的文件创建语言关联（例如许多 JSON 配置文件）。

```json
"file.associations": {
    ".database": "json"
}
```

# 进阶编辑

这里挑选了一些常见的提高编辑效率的技巧。如果键盘快捷键跟你习惯有冲突，可以考虑安装[键映射](https://marketplace.visualstudio.com/search?target=VSCode&category=Keymaps&sortBy=Downloads) 扩展。

## 插入多光标

> Mac: <kbd>opt+cmd+up</kbd> 或 <kbd>opt+cmd+down</kbd>

> Windows: <kbd>ctrl+alt+up</kbd> 或 <kbd>ctrl+alt+down</kbd>

> Linux: <kbd>alt+shift+up</kbd> 或 <kbd>alt+shift+down</kbd>

![multi cursor](/media/multi_cursor.gif)

![multi cursor second example](/media/editingevolved_multicursor.gif)

添加更多的光标到当前选中的地方。

![add cursor to all occurrences of current selection](/media/add_cursor_current_selection.gif)

## 合并行

> Mac: <kbd>ctrl+j</kbd>

> Windows / Linux: 默认没有绑定。 打开快捷方式绑定 `editor.action.joinLines` 到你选择的一个快捷键。

![Join lines](/media/JoinLines.gif)

## 复制当前行到上/下一行

> Mac: <kbd>opt+shift+up</kbd> 或 <kbd>opt+shift+down</kbd>

> Windows / Linux([Issue #5363](https://github.com/Microsoft/vscode/issues/5363)): <kbd>shift+alt+down</kbd> or <kbd>shift+alt+up</kbd>

![copy line down](/media/copy_line_down.gif)

## 收缩/展开选择区域

更多[文档](https://code.visualstudio.com/docs/editor/editingevolved#_selection-multicursor)

> Mac: <kbd>ctrl+shift+cmd+left</kbd> 或 <kbd>ctrl+shift+cmd+right</kbd>

> Windows / Linux: <kbd>shift+alt+left</kbd> 或 <kbd>shift+alt+right</kbd>

![shrink expand selection](/media/shrink_expand_selection.gif)

## 转到文件中的符号

> Mac: <kbd>cmd+shift+o</kbd>

> Windows / Linux: <kbd>ctrl+shift+o</kbd>

![Find by symbol](/media/find_by_symbol.gif)

你可以添加一个冒号`@:`来分组符号

![group symbols by kind](/media/group_symbols_by_kind.png)

## 转到工作区中的符号

> Mac: <kbd>cmd+t</kbd>

> Windows / Linux: <kbd>ctrl+t</kbd>

![go to symbol in workspace](/media/go_to_symbol_in_workspace.png)

## 转到行

> Mac: <kbd>ctrl+g</kbd> or <kbd>cmd+p, :</kbd>

> Windows / Linux: <kbd>ctrl+g</kbd>

![navigate to line](/media/navigate_to_line.gif)

## 撤销光标位

> Mac: <kbd>cmd+u</kbd>

> Windows / Linux: <kbd>ctrl+u</kbd>

![undo cursor position](/media/undo_cursor_position.gif)

## 当前行向上或下移动·

> Mac: <kbd>opt+up</kbd> or <kbd>opt+down</kbd>

> Windows / Linux: <kbd>alt+up</kbd> or <kbd>alt+down</kbd>

![move line up and down](/media/move_line.gif)

## 去除行尾空白

> Mac: <kbd>cmd+k cmd+x</kbd>

> Windows / Linux: <kbd>ctrl+k</kbd> <kbd>ctrl+x</kbd>

![trailing whitespace](/media/trim_whitespace.gif)

## 格式化代码

### 格式化当前选中的源代码

> Mac: <kbd>cmd+k, cmd+f</kbd>

> Windows / Linux: <kbd>ctrl+k, ctrl+f</kbd>

### 格式化当前文档代码

> Windows / Linux: <kbd>shift+alt+f</kbd>

![code formatting](/media/code_formatting.gif)

## 代码折叠

> Mac: <kbd>shift+cmd+\[</kbd> 和 <kbd>shift+cmd+\]</kbd>

> Windows / Linux: <kbd>ctrl+shift+\[</kbd> 和 <kbd>ctrl+shift+\]</kbd>

![code folding](/media/code_folding.gif)

## 选中当前行

> Mac: <kbd>cmd+i</kbd>

> Windows / Linux: <kbd>ctrl+i</kbd>

![select current line](/media/select_current_line.gif)

## 光标跳至行尾

> Mac: <kbd>cmd+up</kbd> 和 <kbd>cmd+down</kbd>

> Windows: <kbd>ctrl+up</kbd> 和 <kbd>ctrl+down</kbd>

> Linux: <kbd>ctrl+home</kbd> 和 <kbd>ctrl+end</kbd>

![navigate to beginning and end of file](/media/beginning_end_file.gif)

## 开启 Markdown 预览

在 Markdown 文件中使用

> Mac: <kbd>shift+cmd+v</kbd>

> Windows / Linux: <kbd>ctrl+shift+v</kbd>

![toggle readme preview](/media/toggle_preview.gif)

## Markdown 预览

在 Markdown 文件中使用

> Mac: <kbd>cmd+k v</kbd>

> Windows / Linux: <kbd>ctrl+k v</kbd>


![markdown sync](/media/markdown-preview-sync.gif)

# 智能提示

无论何时，尝试按下 <kbd>ctrl+space</kbd> 来触发智能建议小部件功能。

![intellisense](/media/intellisense.gif)

你可以查看提供的方法，参数提示及短文档等。

## 一瞥

选择一个符号然后按下 <kbd>alt+f12</kbd>，或者你可以使用上下文菜单（Windows 右键菜单）。

![peek](/media/peek.gif)

## 转到定义

选择一个符号然后按下 <kbd>f12</kbd>，另外你也可以使用上下文菜单或者 <kbd>ctrl+click</kbd> (<kbd>cmd+click</kbd> on macOS)。


![go to definition](/media/goto_definition.gif)

你可以返回到上一个的位置操作**转到** > **后退** 指令或 <kbd>alt+left</kbd> (<kbd>ctrl+-</kbd> on macOS)。

## 查找所有申明

选择一个符号然后按下 <kbd>shift+f12</kbd>，或者可以使用环境菜单。

![find all references](/media/find_all_references.gif)

## 重命名 Symbol

选择一个 symbol 然后按下 <kbd>f2</kbd>，你也可以使用环境菜单。

![rename symbol](/media/rename_symbol.gif)

## .eslintrc.json

安装 [ESLint 插件](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)。配置你喜欢的 linter，具体请参考[这里](http://eslint.org/docs/user-guide/configuring).

下面是使用 ES6 的配置

```json
{
    "env": {
        "browser": true,
        "commonjs": true,
        "es6": true,
        "node": true
    },
    "parserOptions": {
        "ecmaVersion": 6,
        "sourceType": "module",
        "ecmaFeatures": {
            "jsx": true,
            "classes": true,
            "defaultParams": true
        }
    },
    "rules": {
        "no-const-assign": 1,
        "no-extra-semi": 0,
        "semi": 0,
        "no-fallthrough": 0,
        "no-empty": 0,
        "no-mixed-spaces-and-tabs": 0,
        "no-redeclare": 0,
        "no-this-before-super": 1,
        "no-undef": 1,
        "no-unreachable": 1,
        "no-use-before-define": 0,
        "constructor-super": 1,
        "curly": 0,
        "eqeqeq": 0,
        "func-names": 0,
        "valid-typeof": 1
    }
}
```

## package.json

查看你 `package.json` 文件的智能提示

![package json intellisense](/media/package_json_intellisense.gif)

## Emmet 语法

[更多支持 Emmt 的语法](https://code.visualstudio.com/docs/languages/html#_emmet-snippets).

![emmet syntax](/media/emmet_syntax.gif)

# 代码片段

## 建立自定义代码片段

**文件** > **首选项** > **用户代码片段**，选择相关语言建立代码片段。

```json
"create component": {
    "prefix": "component",
    "body": [
        "class $1 extends React.Component {",
        "",
        "	render() {",
        "		return ($2);",
        " 	}",
        "",
        "}"
    ]
},
```

查看更多详细内容关于 [建立用户代码片段](https://code.visualstudio.com/docs/editor/userdefinedsnippets)。

# Git 集成

VS Code 默认内部集成 Git ，你也可以在扩展商店安装其他的源码版本管理系统。这一部分只作 VS Code 内部集成的 Git 介绍，其他源码版本管理工具也可参考，大同小异而已。

## Diffs 代码差异比较

点击编辑器左侧活动栏上的源代码管理按钮(<kbd>ctrl+shift+G</kbd>)，然后点击列表上的 M 按钮可以并排查看文件修改的对比。

![git icon](/media/git_icon.png)

**并排视图**

默认是纵向并排比较代码差异

![git diff side by side](/media/git_side_by_side.png)

**内联视图**

在并排对比视图状态下可以通过点击右上角**更多**按钮选择**切换到内联视图**

![more git button](/media/more_button.png)

![git inline](/media/git_inline.png)

如果你更喜欢内联视图，可以设置 `"diffEditor.renderSideBySide": false`。


**Review Pane**

在对比视图中通过 `F7` 和 `Shift+F7` 来切换到不同的代码区块，通过箭头键和 `Enter` 键可以定位行.

![diff_review_pane](/media/diff_review_pane.png)


**编辑暂存变更**

你可以在比较视图中直接编辑暂存变更


## 分支

通过状态栏可以方便的切换 Git 分支。

![switch branches](/media/switch_branches.gif)

## 暂存

**暂存所有文件**

鼠标悬停在有数字的文件上点击加号按钮。


![git stage all](/media/git_stage_all.gif)

**暂存某个文件**

在**命令面板**选择**暂存所选范围**暂存文件的一部分


![git stage selected](https://cloud.githubusercontent.com/assets/1926584/23407797/ebeefbb4-fdc5-11e6-8ca1-c4c6c056a8fd.png)

## 撤消上次提交

![undo last commit](/media/undo_last_commit.gif)

## 查看 Git 输出

VS Code 可以方便的查看 Git 指令是否有效的执行，这对学习 Git 或调试困难的 issue 很有帮助。

> Mac: <kbd>shift+cmd+u</kbd>

> Windows / Linux: <kbd>ctrl+shift+u</kbd>

在输出窗口下拉菜单选择 **Git** 运行 `toggleOutput`。

## Gutter 指示器

Gutter 指示器功能可以让你在编辑器编辑区看到源码被改动过的一些痕迹，详细内容请看[这里](https://code.visualstudio.com/docs/editor/versioncontrol#_gutter-indicators)。

* 一个红色三角形表示被删除的行
* 一个绿色的竖条表示新增的行
* 一个蓝色竖条表示修改过的行

![git gutter indicators](/media/editingevolved_gutter.png)

## 解决合并冲突

在合并分支时，在活动栏点击源代码管理按钮

![git icon](/media/git_icon.png)

## 设置 VS Code 为默认合并分支工具

```bash
git config --global merge.tool code
```

# 调试

## 配置调试器

按 <kbd>f1</kbd> 选择 **Debug: Open launch.json** 环境，会产生一个 `lanch.json` 文件。如果要为 Node.js 和其他环境配置立即可用的，可能需要一些其他语言的配置，具体内容请参考[文档](https://code.visualstudio.com/docs/editor/debugging)

![configure debugging](/media/configure_debug.gif)

## 断点和单步调试

紧挨着行号放置断点，点击调试小部件窗口的绿色前进三角按钮开始调试。

![debug](/media/node_debug.gif)

## 数据审查

在调试面板和调试控制台中检查变量

![data inspection](/media/debug_data_inspection.gif)

## 内联值

你可以通过设置 `"debug.inlineValues": true` 打开在调试器中来查看提供的值这个功能，这个功能还处于实验阶段所以默认是关闭的。

# 运行任务

## 自动获取任务

Select **Tasks** from the top-level menu, run the command **Configure Tasks...**, then select the type of task you'd like to run.
This will generate a `task.json` file with content like the following. See the Tasks [documentation](https://go.microsoft.com/fwlink/?LinkId=733558) for more details.

```json
{
    // See http://go.microsoft.com/fwlink/?LinkId=733558
    // for the documentation about the tasks.json format
    "version": "0.1.0",
    "command": "npm",
    "isShellCommand": true,
    "showOutput": "always",
    "suppressTaskName": true,
    "tasks": [
        {
            "taskName": "install",
            "args": ["install"]
        },
        {
            "taskName": "build",
            "args": ["run", "build"]
        }
    ]
}
```

有一些偶然的 issue 会自动产生，查阅文档可以让你事半功倍哦。


## 从任务菜单运行任务

从顶层菜单选择**任务**，选择**运行任务...**命令，接着选择你想运行的人物。选择**终止任务...** 停止任务运行。

![task runner](/media/task_runner.gif)


## 其他资源

* [vscode 官方文档](https://code.visualstudio.com/docs)
* [react sample app](https://github.com/Microsoft/vscode-react-sample)
* [awesome vscode](https://github.com/viatsko/awesome-vscode)
