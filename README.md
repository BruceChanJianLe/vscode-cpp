# vscode CPP

This repository demonstrates the setting up and usage of cpp static check tools.

## Extensions

**C/C++ Advanced Lint**:  

Please enable everything that you see for cppcheck in the settings [ctrl + ,]
Set it up as follow:
```json
{
    "python.defaultInterpreterPath": "/usr/bin/python3",
    "editor.lineNumbers": "relative",
    "cmake.configureOnOpen": true,
    "cmake.buildDirectory": "${workspaceFolder}/build-vscode",
    "testMate.cpp.log.userId": "82cdd95340a0c3075fb44e7c043c393e1bdb7a70",
    "testMate.cpp.log.logSentry": "disable_3",
    "vim.leader": "<space>",
    "vim.vimrc.enable": true,
    "vim.vimrc.path": "/home/chanjl/.vimrc",
    "scm.defaultViewMode": "tree",
    "vim.normalModeKeyBindingsNonRecursive": [
            {
                "before": ["<leader>", "w"],
                "after": [":wa"]
            },
            {
                "before": ["<leader>", "x"],
                "after": [":x"]
            },
            {
                "before": ["<leader>", "r"],
                "after": ["%s///gc<Left><Left><Left>"]
            },
            {
                "before": ["<leader>", "<leader>", "r"],
                "after": ["%s///g<Left><Left>"]
            },
            {
                "before": ["<leader>", "e"],
                "after": [":e!"]
            },
            {
                "before": ["<leader>", "q"],
                "commands": ["workbench.action.closeActiveEditor"]
            },
            {
                "before": ["<leader>", "z"],
                "commands": ["workbench.action.toggleEditorWidths"] 
            }
    ],
    "C_Cpp.default.intelliSenseMode": "clang-x86",
    "clangd.path": "/home/chanjl/.config/Code/User/globalStorage/llvm-vs-code-extensions.vscode-clangd/install/10.0.0/clangd_10.0.0/bin/clangd",
    "editor.renderWhitespace": "all",
    "C_Cpp.updateChannel": "Insiders",
    "window.zoomLevel": 0,
    "ros.distro": "melodic",
    "xml.symbols.maxItemsComputed": 10000,
    "vim.commandLineModeKeyBindings": [
    
    ],
    "[makefile]": {
        "editor.insertSpaces": false
    },
    "c-cpp-flylint.flexelint.enable": false,
    "c-cpp-flylint.clang.standard": [
        "c++11",
    ],
    "cppcheck.severity": "",
    "c-cpp-flylint.cppcheck.force": true,
    "c-cpp-flylint.cppcheck.inconclusive": true,
    "c-cpp-flylint.cppcheck.verbose": true,
    "c-cpp-flylint.debug": true,
    "c-cpp-flylint.cppcheck.standard": [
        "c++11",
    ],
}
```

For local include paths please add the following:
```json
{
    "python.autoComplete.extraPaths": [
        "/home/chanjl/isera2_prep_box/isera2_new_struct/devel/lib/python2.7/dist-packages",
        "/home/chanjl/isera2_prep_box/scout_msgs_ws/devel/lib/python2.7/dist-packages",
        "/home/chanjl/isera2_prep_box/vision_ws/devel/lib/python2.7/dist-packages",
        "/opt/ros/melodic/lib/python2.7/dist-packages"
    ],
    "c-cpp-flylint.clang.includePaths": [
        // It will be better to not include the ROS headers and eigen3
        "/opt/ros/melodic/include",
        "${workspaceFolder}/i2r_sliding_autonomy_server/include",
        "${workspaceFolder}/../../devel/include/",
        "/usr/include/eigen3"
    ],
    "c-cpp-flylint.cppcheck.includePaths": [
        // It will be better to not include the ROS headers and eigen3
        "/opt/ros/melodic/include",
        "${workspaceFolder}/i2r_sliding_autonomy_server/include",
        "${workspaceFolder}/../../devel/include/",
        "/usr/include/eigen3"
    ]
}
```
