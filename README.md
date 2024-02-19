# vscode-settings-and-keybindings
My Vim focused Vscode settings.json and keybindings.json


## Vim keybindings and settings
[Refer to complete settings.json](https://github.com/JaiminBrahmbhatt/vscode-settings-and-keybindings/blob/main/settings.json)

```
    // vim settings
    "extensions.experimental.affinity": {
        "vscodevim.vim": 1
    },
    "vim.easymotion": true, // easy motions plugin to move around
    "vim.highlightedyank.enable": true,
    "vim.history": 1000,
    "vim.hlsearch": false,
    "vim.leader": "<space>", // allows you to easyily create keybindings in vim you will see some example below
    "vim.smartRelativeLine": true, // enable rlnu when in NORMAL mode and VISUAL mode disables in INSERT mode
    "vim.surround": true, // enable vim surround plugin https://github.com/VSCodeVim/Vim?tab=readme-ov-file#vim-surround

    "vim.insertModeKeyBindings": [
        {
            "before": [
                "j",
                "k",
            ],
            "after": [
                "<Esc>"
            ]
        },
    ],

    "vim.normalModeKeyBindings": [
        {
            "before": [
                "g",
                "p",
                "d"
            ],
            "commands": [
                "editor.action.peekDefinition"
            ]
        },
        {
            "before": [
                "g",
                "i"
            ],
            "commands": [
                "editor.action.goToImplementation"
            ]
        },
        {
            "before": [
                "g",
                "p",
                "i"
            ],
            "commands": [
                "editor.action.peekImplementation"
            ]
        },
        {
            "before": [
                "g",
                "q"
            ],
            "commands": [
                "editor.action.quickFix"
            ]
        },
        {
            "before": [
                "g",
                "r"
            ],
            "commands": [
                "editor.action.referenceSearch.trigger"
            ]
        },
        {
            "before": [
                "g",
                "t"
            ],
            "commands": [
                "editor.action.goToTypeDefinition"
            ]
        },
        {
            "before": [
                "g",
                "p",
                "t"
            ],
            "commands": [
                "editor.action.peekTypeDefinition"
            ]
        },
        // easy move from one error/lint/info to another
        {
            "before": [
                "g",
                "]"
            ],
            "commands": [
                "editor.action.marker.next"
            ]
        },
        {
            "before": [
                "g",
                "["
            ],
            "commands": [
                "editor.action.marker.previous",
            ]
        },
    ],

    "vim.normalModeKeyBindingsNonRecursive": [
        // quick bind for easymotions
        {
            "before": [
                "<Leader>",
                "<Leader>",
                "b"
            ],
            "after": [
                "leader",
                "leader",
                "leader",
                "b",
                "d",
                "w"
            ]
        },
        // Switch between open buffers(files)
        {
            "before": [
                "<S-h>"
            ],
            "commands": [
                ":bprevious"
            ]
        },
        {
            "before": [
                "<S-l>"
            ],
            "commands": [
                ":bnext"
            ]
        },
        // Switch between panes
        {
            "before": [
                "leader",
                "h"
            ],
            "commands": [
                "workbench.action.focusLeftGroup"
            ]
        },
        {
            "before": [
                "leader",
                "j"
            ],
            "commands": [
                "workbench.action.focusBelowGroup"
            ]
        },
        {
            "before": [
                "leader",
                "k"
            ],
            "commands": [
                "workbench.action.focusAboveGroup"
            ]
        },
        {
            "before": [
                "leader",
                "l"
            ],
            "commands": [
                "workbench.action.focusRightGroup"
            ]
        },
        {
            "before": [
                "<Leader>",
                "t",
                "t"
            ],
            "commands": [
                ":tabnew"
            ]
        },
        {
            "before": [
                "<Leader>",
                "t",
                "n"
            ],
            "commands": [
                ":tabnext"
            ]
        },
        {
            "before": [
                "<Leader>",
                "t",
                "p"
            ],
            "commands": [
                ":tabprev"
            ]
        },
        {
            "before": [
                "<Leader>",
                "t",
                "o"
            ],
            "commands": [
                ":tabo"
            ]
        }
    ],

    "vim.visualModeKeyBindings": [
        {
            "before": [
                ">"
            ],
            "commands": [
                "editor.action.indentLines"
            ]
        },
        {
            "before": [
                "<"
            ],
            "commands": [
                "editor.action.outdentLines"
            ]
        },
    ],

```

## Visuals and feel of VSCode
```
    "debug.toolBarLocation": "docked",
    "editor.accessibilitySupport": "off",
    "editor.bracketPairColorization.enabled": true,
    "editor.cursorSmoothCaretAnimation": "on",
    "editor.cursorBlinking": "phase",

    "editor.fontFamily": "Consolas, Monaco, 'Courier New', monospace",
    "editor.fontSize": 14,
    "editor.guides.bracketPairs": true,
    "editor.minimap.autohide": true,
    "editor.minimap.enabled": false,
    "editor.scrollbar.horizontal": "hidden",
    "editor.scrollbar.vertical": "hidden",
    "editor.scrollBeyondLastLine": false,
    "editor.smoothScrolling": true,
    "terminal.integrated.fontSize": 12,
    "window.commandCenter": false,
    "window.zoomLevel": 1,
    "workbench.list.smoothScrolling": true,
    "workbench.tree.renderIndentGuides": "always",
```

## Misc
```
    // editor
    "editor.colorDecorators": true,
    "editor.formatOnPaste": true,
    "editor.formatOnType": true,
    "editor.inlineSuggest.allowSuggestOnTriggerCharacters": true,
    "editor.linkedEditing": true,
    "editor.multiCursorModifier": "ctrlCmd",
    "editor.stickyScroll.enabled": true,
    "editor.suggest.insertMode": "replace",
    "editor.suggestSelection": "first",
    "editor.suggest.snippetsPreventQuickSuggestions": false,
    "editor.tabSize": 2,
    "[markdown]": {
        "files.trimTrailingWhitespace": false
    },
    "terminal.external.osxExec": "iTerm.app",
    "terminal.integrated.cursorBlinking": true,
    "terminal.integrated.cursorStyle": "line",
    "terminal.integrated.defaultProfile.osx": "zsh",
    "terminal.integrated.defaultProfile.linux": "zsh",
    "terminal.integrated.fontFamily": "MesloLGS NF",
    "terminal.integrated.scrollback": 100000,
    "terminal.integrated.tabs.enabled": true,

    // Misc
    "explorer.confirmDelete": false,
    "explorer.confirmDragAndDrop": false,
    "extensions.autoUpdate": "onlyEnabledExtensions",
    "extensions.autoCheckUpdates": true,
    "files.trimTrailingWhitespace": true,
    "notebook.formatOnSave.enabled": true,
    "workbench.colorTheme": "GitHub Dark",
    "workbench.layoutControl.enabled": false,
    "workbench.startupEditor": "none",
    "workbench.productIconTheme": "icons-carbon",
    "window.nativeTabs": true,
    "window.restoreWindows": "none",
    "terminal.integrated.shellIntegration.history": 1000,
    "terminal.integrated.systemd.shouldUse": true,
    "terminal.integrated.env.osx": {},
```

## Color Customizations of VScode

```
    "workbench.colorCustomizations": {
        "tab.activeBorderTop": "#12ff00",
        "tree.indentGuidesStroke": "#999999",
        // terminal customization
        "terminalCursor.background": "#282a36",
        "terminalCursor.foreground": "#97979b",
        "terminal.selectionBackground": "#97979b33",
        "terminal.foreground": "#eff0eb",
        "terminal.ansiBlack": "#282a36",
        "terminal.ansiRed": "#ff5c57",
        "terminal.ansiGreen": "#5af78e",
        "terminal.ansiYellow": "#f3f99d",
        "terminal.ansiBlue": "#57c7ff",
        "terminal.ansiMagenta": "#ff6ac1",
        "terminal.ansiCyan": "#9aedfe",
        "terminal.ansiWhite": "#f1f1f0",
        "terminal.ansiBrightBlack": "#686868",
        "terminal.ansiBrightRed": "#ff5c57",
        "terminal.ansiBrightGreen": "#5af78e",
        "terminal.ansiBrightYellow": "#f3f99d",
        "terminal.ansiBrightBlue": "#57c7ff",
        "terminal.ansiBrightMagenta": "#ff6ac1",
        "terminal.ansiBrightCyan": "#9aedfe",
        "terminal.ansiBrightWhite": "#eff0eb"
    },
```
