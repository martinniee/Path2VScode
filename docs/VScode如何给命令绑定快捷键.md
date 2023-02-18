# VScode如何给命令绑定快捷键

步骤
1. `ctrl + shift + p` 打开命令面板
2. 输入 `workbench.action.openGlobalKeybindingsFile`
3. 进入 `<$HOME>\AppData\Roaming\Code\User\keybindings.json`

编辑内容如下格式

```json
// 将键绑定放在此文件中以覆盖默认值auto[]
[
    {
        "key": "alt+v",
        "command": "workbench.action.toggleSidebarVisibility"
    },
    {
        "key": "ctrl+b",
        "command": "-workbench.action.toggleSidebarVisibility"
    },
    {
        "key": "shift+a",
        "command": "git.stage"
    }
]
```
说明：
- `"key": "ctrl+b",` ： 表示快捷键字段，`ctrl+b`表示设置快捷键为 `ctrl + b`
-  `"command": "git.stage"` : 表示命令字段， `git.stage` 表示绑定快捷键的命令。 TIP: 输入` git.` 会弹出选项框提供很多git相关的命令

上述设置后，在编辑器内按 `ctrl + b` 就会执行 `git add` 命令，将当前的文件跟踪（暂存）

## Reference

- https://stackoverflow.com/a/68358345








