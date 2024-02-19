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
