# Integrated Terminal

1. The Integrated Terminal in VS Code
    1. What we’ll cover
        1. How to open and use the Integrated Terminal
        2. Working with multiple terminals
        3. How to choose your integrated shell
    2. Resources
        1. [VS Code Docs Integrated Terminal](https://code.visualstudio.com/docs/editor/integrated-terminal)
    3. Pro Tips
        1. Some prefer to use an outside terminal rather than the one built into VS Code.  Give the integrated terminal a try and decide for yourself.
        2. `ctrlCmd + Tilde` – toggle integrated terminal
4. Customizing Your Terminal Setup Part 2
    1. What we’ll cover
        1. How to customize shortcuts to interact with terminal windows like files in the editor(opening, closing, and switching between terminal windows)
    2. Resources
        1. [VS Code Docs Integrated Terminal](https://code.visualstudio.com/docs/editor/integrated-terminal)
    3. Pro Tips
        1. Using the above configuration can make it much quicker and easier to work with multiple terminal windows.

```json
{
    "key": "ctrl+tab",
    "command": "workbench.action.terminal.focusNext",
    "when": "terminalFocus"
},
{
    "key": "ctrl+shift+tab",
    "command": "workbench.action.terminal.focusPrevious",
    "when": "terminalFocus"
},
{
    "key": "cmd+n",
    "command": "workbench.action.terminal.new",
    "when": "terminalFocus"
},
{
    "key": "cmd+w",
    "command": "workbench.action.terminal.kill",
    "when": "terminalFocus"
},
{
    "key": "cmd+r",
    "command": "workbench.action.terminal.rename",
    "when": "terminalFocus"
}
```
