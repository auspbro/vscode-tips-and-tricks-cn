
# [VS Code](https://code.visualstudio.com) 提升编码效率的技巧集

# 内容目录

1. <a href="#入门">入门</a>
2. <a href="#个性化自定义">个性化自定义</a>
3. <a href="#extensions">插件扩展</a>
4. <a href="#file-and-folder-management">文件及文件夹管理</a>
5. <a href="#editing-hacks">进阶编辑</a>
6. <a href="#intellisense">智能提示</a>
7. <a href="#snippets">创建代码片段</a>
8. <a href="#git-integration">Git 集成</a>
9. <a href="#debugging">调试</a>
10. <a href="#task-runner">Task runner</a>
11. <a href="#other-resources">其他资源</a>

> 文中内容提到的快捷键操作有可能和最新版本有所出入，最新版本的键盘快捷键请参考[这里](https://code.visualstudio.com/docs/getstarted/keybindings)

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

You can open multiple files from **Quick Open** by pressing the Right arrow key. This will open the currently selected file in the background and you can continue selecting files from **Quick Open**.

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

Workspace specific files are in `.vscode`. For example, `tasks.json` for the Task Runner and `launch.json` for the debugger.
·

## 状态栏

**错误和警告**

> Mac: <kbd>shift+cmd+m</kbd>

> Windows / Linux: <kbd>ctrl+shift+m</kbd>

快速跳转到项目出错和警告的位置

循环通过错误 <kbd>f8</kbd> or <kbd>shift+f8</kbd>

![errors and warnings](/media/Errors_Warnings.gif)

You can filter problems by type ('errors', 'warnings') or text matching.

**更换语言模式**

> Mac: <kbd>cmd+k m</kbd>

> Windows / Linux: <kbd>ctrl+k m</kbd>

![change syntax](/media/change_syntax.gif)

If you want to persist the new language mode for that file type, you can use the **Configure File Association for ...** command to associate the current file extension with an installed language.

# 自定义

·通过自定义 VS Code,你可以做更多事情

* 更换主题
* 更换键盘快捷键
* 调整设定
* 添加 Json 许可
* 创建代码片段
* 安装扩展

Check out the full [documentation](https://code.visualstudio.com/docs/getstarted/settings).

## 更改主题

打开 **命令面板** 输入"themes". 你可以在扩展市场安装更多主题。

![Preview themes](/media/PreviewThemes.gif)

另外你可以安装更改文件图标的主题

![File icon themes](/media/PreviewFileIconThemes.gif)

## 更换键盘快捷键

### Keyboard Reference Sheets
### 键盘快捷键参考文档

对应的平台的快捷键参考文档 ([macOS](https://go.microsoft.com/fwlink/?linkid=832143), [Windows](https://go.microsoft.com/fwlink/?linkid=832145), [Linux](https://go.microsoft.com/fwlink/?linkid=832144)).

![Keyboard Reference Sheet](/media/KeyboardReferenceSheet.png)

### 键映射

如果你习惯于某种编辑器的快捷键，可以安装快捷键扩展到 VS Code 来导入你常用的编辑器的快捷键。 选择 **首选项** > **键映射扩展** 去 [Marketplace](https://marketplace.visualstudio.com/search?target=VSCode&category=Keymaps&sortBy=Downloads) 查看当前列表。 比较流行的一些:

- [Vim](https://marketplace.visualstudio.com/items?itemName=vscodevim.vim)
- [Sublime Text Keymap](https://marketplace.visualstudio.com/items?itemName=ms-vscode.sublime-keybindings)
- [Emacs Keymap](https://marketplace.visualstudio.com/items?itemName=hiro-sun.vscode-emacs)
- [Atom Keymap](https://marketplace.visualstudio.com/items?itemName=ms-vscode.atom-keybindings)

### 自定义键盘快捷键

打开 **命令面板** 输入"keyboard shortcuts" 现在可以在文件的右侧添加你自己的组合键了。

![customize keyboard shortcuts](/media/KeyboardShortcuts.gif)

查看更多 [· for Visual Studio Code](https://code.visualstudio.com/docs/getstarted/keybindings).

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

You can also toggle Auto Save from the top-level menu with the **File** > **Auto Save**.
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

Enabled by default for many files. Create your own schema and validation in `settings.json`

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

活着在你的工作区定义一个 schema

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

# 扩展

## 查找扩展

1. 在 VS Code [市场](https://marketplace.visualstudio.com/vscode).
2. 在 VS Code 内搜索
3. 查看扩展推荐
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

- [Official documentation](https://code.visualstudio.com/docs/editor/integrated-terminal)
- [Mastering VS Code's Terminal article](http://www.growingwiththeweb.com/2017/03/mastering-vscodes-terminal.html)


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

## 免干扰模式

> Mac: <kbd>cmd+k z</kbd>

> Windows / Linux: <kbd>ctrl+k z</kbd>

![zen mode](/media/zen_mode.gif)

Enter distraction free Zen mode.

## 拆分编辑器

> Mac: <kbd>cmd+\\</kbd> 或者 <kbd>cmd</kbd> 然后从文件管理器点击一个文件

> Windows / Linux: <kbd>ctrl+\\</kbd>

> Linux: <kbd>ctrl+2</kbd>

![split editors](/media/split_editor.gif)

You can use drag and drop editors to create new editor groups and move editors between groups.

## 在多页编辑器之间切换

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


Navigate back.
操作历史往后回溯。

> Mac: <kbd>ctrl+-</kbd>

> Windows / Linux: <kbd>alt+left</kbd>

Navigate Forward.
操作历史向前回溯。

> Mac: <kbd>ctrl+shift+-</kbd>

> Windows / Linux: <kbd>alt+right</kbd>

![navigate history](/media/navigate_history.gif)

## Navigate to a file
## 回溯文件

> Mac: <kbd>cmd+e</kbd> or <kbd>cmd+p</kbd>

> Windows / Linux: <kbd>ctrl+e</kbd> or <kbd>ctrl+p</kbd>

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

## Multi cursor selection
## 多光标选择

> Mac: <kbd>opt+cmd+up</kbd> 或者 <kbd>opt+cmd+down</kbd>

> Windows: <kbd>ctrl+alt+up</kbd> 或者 <kbd>ctrl+alt+down</kbd>

> Linux: <kbd>alt+shift+up</kbd> 或者 <kbd>alt+shift+down</kbd>

![multi cursor](/media/multi_cursor.gif)

![multi cursor second example](/media/editingevolved_multicursor.gif)

Add more cursors to current selection.·

![add cursor to all occurrences of current selection](/media/add_cursor_current_selection.gif)

## Join line

> Mac: <kbd>ctrl+j</kbd>

> Windows / Linux: Not bound by default. Open Keyboard Shortcuts and bind `editor.action.joinLines` to a shortcut of your choice.

![Join lines](/media/JoinLines.gif)

## Copy line up / down

> Mac: <kbd>opt+shift+up</kbd> or <kbd>opt+shift+down</kbd>

> Windows / Linux([Issue #5363](https://github.com/Microsoft/vscode/issues/5363)): <kbd>shift+alt+down</kbd> or <kbd>shift+alt+up</kbd>

![copy line down](/media/copy_line_down.gif)

## Shrink / expand selection

More in [documentation](https://code.visualstudio.com/docs/editor/editingevolved#_selection-multicursor)

> Mac: <kbd>ctrl+shift+cmd+left</kbd> or <kbd>ctrl+shift+cmd+right</kbd>

> Windows / Linux: <kbd>shift+alt+left</kbd> or <kbd>shift+alt+right</kbd>

![shrink expand selection](/media/shrink_expand_selection.gif)

## Go to Symbol in File

> Mac: <kbd>cmd+shift+o</kbd>

> Windows / Linux: <kbd>ctrl+shift+o</kbd>

![Find by symbol](/media/find_by_symbol.gif)

You can group the symbols by kind by adding a colon, `@:`.

![group symbols by kind](/media/group_symbols_by_kind.png)

## Go to Symbol in Workspace

> Mac: <kbd>cmd+t</kbd>

> Windows / Linux: <kbd>ctrl+t</kbd>

![go to symbol in workspace](/media/go_to_symbol_in_workspace.png)

## Navigate to a specific line

> Mac: <kbd>ctrl+g</kbd> or <kbd>cmd+p, :</kbd>

> Windows / Linux: <kbd>ctrl+g</kbd>

![navigate to line](/media/navigate_to_line.gif)

## Undo cursor position

> Mac: <kbd>cmd+u</kbd>

> Windows / Linux: <kbd>ctrl+u</kbd>

![undo cursor position](/media/undo_cursor_position.gif)

## Move line up and down

> Mac: <kbd>opt+up</kbd> or <kbd>opt+down</kbd>

> Windows / Linux: <kbd>alt+up</kbd> or <kbd>alt+down</kbd>

![move line up and down](/media/move_line.gif)

## Trim trailing whitespace

> Mac: <kbd>cmd+k cmd+x</kbd>

> Windows / Linux: <kbd>ctrl+k</kbd> <kbd>ctrl+x</kbd>

![trailing whitespace](/media/trim_whitespace.gif)

## Code formatting

### Currently selected source code

> Mac: <kbd>cmd+k, cmd+f</kbd>

> Windows / Linux: <kbd>ctrl+k, ctrl+f</kbd>

### Whole document format

> Windows / Linux: <kbd>shift+alt+f</kbd>

![code formatting](/media/code_formatting.gif)

## Code folding

> Mac: <kbd>shift+cmd+\[</kbd> and <kbd>shift+cmd+\]</kbd>

> Windows / Linux: <kbd>ctrl+shift+\[</kbd> and <kbd>ctrl+shift+\]</kbd>

![code folding](/media/code_folding.gif)

## Select current line

> Mac: <kbd>cmd+i</kbd>

> Windows / Linux: <kbd>ctrl+i</kbd>

![select current line](/media/select_current_line.gif)

## Navigate to beginning and end of file

> Mac: <kbd>cmd+up</kbd> and <kbd>cmd+down</kbd>

> Windows: <kbd>ctrl+up</kbd> and <kbd>ctrl+down</kbd>

> Linux: <kbd>ctrl+home</kbd> and <kbd>ctrl+end</kbd>

![navigate to beginning and end of file](/media/beginning_end_file.gif)

## Open Markdown Preview

In a Markdown file, use

> Mac: <kbd>shift+cmd+v</kbd>

> Windows / Linux: <kbd>ctrl+shift+v</kbd>

![toggle readme preview](/media/toggle_preview.gif)

## Side by Side Markdown Edit and Preview

In a Markdown file, use

> Mac: <kbd>cmd+k v</kbd>

> Windows / Linux: <kbd>ctrl+k v</kbd>

Special bonus: The preview will now sync.

![markdown sync](/media/markdown-preview-sync.gif)

# IntelliSense

Anytime, try <kbd>ctrl+space</kbd> to trigger the Suggestions widget.

![intellisense](/media/intellisense.gif)

You can view available methods, parameter hints, short documentation, etc.

## Peek

Select a symbol then type <kbd>alt+f12</kbd>. Alternatively, you can use the context menu.

![peek](/media/peek.gif)

## Go to Definition

Select a symbol then type <kbd>f12</kbd>. Alternatively, you can use the context menu or <kbd>ctrl+click</kbd> (<kbd>cmd+click</kbd> on macOS).

![go to definition](/media/goto_definition.gif)

You can go back to your previous location with the **Go** > **Back** command or <kbd>alt+left</kbd> (<kbd>ctrl+-</kbd> on macOS).

## Find All References

Select a symbol then type <kbd>shift+f12</kbd>. Alternatively, you can use the context menu.

![find all references](/media/find_all_references.gif)

## Rename Symbol

Select a symbol then type <kbd>f2</kbd>. Alternatively, you can use the context menu.

![rename symbol](/media/rename_symbol.gif)

## .eslintrc.json

Install the [ESLint extension](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint). Configure
your linter however you'd like. Specification is [here](http://eslint.org/docs/user-guide/configuring).

Here is configuration to use ES6.

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

See IntelliSense for your `package.json` file.

![package json intellisense](/media/package_json_intellisense.gif)

## Emmet syntax

[Support for Emmet syntax](https://code.visualstudio.com/docs/languages/html#_emmet-snippets).

![emmet syntax](/media/emmet_syntax.gif)

# Snippets

## Create custom snippets

**File** > **Preferences** > **User Snippets**, select the language, and create a snippet.

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

See more details in [Creating your own Snippets](https://code.visualstudio.com/docs/editor/userdefinedsnippets).

# Git Integration

Git integration comes with VS Code "in-the-box". You can install other SCM provider from the extension Marketplace. This section describes the Git integration but much of the UI and gestures are shared by other SCM providers.

## Diffs

Click the Source Control button in the Activity Bar then select the file to diff.

![git icon](/media/git_icon.png)

**Side by side**

Default is side by side diff.

![git diff side by side](/media/git_side_by_side.png)

**Inline view**

Toggle inline view by clicking the **More** (...) button in the top right and selecting **Switch to Inline View**.

![more git button](/media/more_button.png)

![git inline](/media/git_inline.png)

If you prefer the inline view, you can set `"diffEditor.renderSideBySide": false`.


**Review Pane**

Navigate through diffs with `F7` and `Shift+F7`. This will present them in a unified patch format. 
Lines can be navigated with arrow keys and pressing `Enter` will jump back in the diff editor and the selected line.

![diff_review_pane](/media/diff_review_pane.png)


**Edit pending changes**

You can make edits directly in the pending changes of the diff view.


## Branches

Easily switch between Git branches via the Status Bar.

![switch branches](/media/switch_branches.gif)

## Staging

**Stage all**

Hover over the number of files and click the plus button.

![git stage all](/media/git_stage_all.gif)

**Stage selected**

Stage a portion of a file by selecting that file (using the arrows) and then choosing **Stage Selected Ranges** from the **Command Palette**.

![git stage selected](https://cloud.githubusercontent.com/assets/1926584/23407797/ebeefbb4-fdc5-11e6-8ca1-c4c6c056a8fd.png)

## Undo last commit

![undo last commit](/media/undo_last_commit.gif)

## See Git output

VS Code makes it easy to see what Git commands are actually running. This is helpful when learning Git or debugging a difficult source control issue.

> Mac: <kbd>shift+cmd+u</kbd>

> Windows / Linux: <kbd>ctrl+shift+u</kbd>

to run `toggleOutput`. Select **Git** in the drop-down.

## Gutter indicators

View diff decorations in editor. See [documentation](https://code.visualstudio.com/docs/editor/versioncontrol#_gutter-indicators) for more details.

![git gutter indicators](/media/editingevolved_gutter.png)

## Resolve merge conflicts

During a merge, click the Source Control button in the Activity Bar and make changes in the diff view.

![git icon](/media/git_icon.png)

## Setup VS Code as default merge tool

```bash
git config --global merge.tool code
```

# Debugging

## Configure debugger

<kbd>f1</kbd> and select **Debug: Open launch.json**, select the environment. This will generate a `launch.json` file. Works out of the box as expected for Node.js and other environments. May need some additional configuration for other languages. See [documentation](https://code.visualstudio.com/docs/editor/debugging) for more details.

![configure debugging](/media/configure_debug.gif)

## Breakpoints and stepping through

Place breakpoints next to the line number. Navigate forward with the Debug widget.

![debug](/media/node_debug.gif)

## Data inspection

Inspect variables in the Debug panels and in the console.

![data inspection](/media/debug_data_inspection.gif)

## Inline values

You can set `"debug.inlineValues": true` to see variable values inline in the debugger. This feature is experimental and disabled by default.

# Task Runner

## Auto detect tasks

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

There are occasionally issues with auto generation. Check out the documentation for getting things to work properly.

## Run tasks from the Tasks menu

Select **Tasks** from the top-level menu, run the command **Run Task...**, and select the task you want to run. Terminate the running task by running the command **Terminate Task...**

![task runner](/media/task_runner.gif)


## Other Resources

* [vscode official docs](https://code.visualstudio.com/docs)
* [react sample app](https://github.com/Microsoft/vscode-react-sample)
* [awesome vscode](https://github.com/viatsko/awesome-vscode)
