#### 是什么

PyCharm里面创建的项目，迁移到VSCode里面，运行的时候找不到模块

#### 为什么

python路径里没有当前工作空间，对应的目录，所以就找不到

#### 怎么做

把工作空间对应的目录，添加到python路径下面即可

文件目录：“根目录\.vscode\settings.json”

*注意：*文件名也要一模一样，否则无法生效

```
{
    "terminal.integrated.env.osx": {
        "PYTHONPATH": "${workspaceFolder}/"
    },
    "terminal.integrated.env.linux": {
        "PYTHONPATH": "${workspaceFolder}/"
    },
    "terminal.integrated.env.windows": {
        "PYTHONPATH": "${workspaceFolder}/"
    }
}
```

![1](https://github.com/hyqing/athena/raw/master/image/settings.png)

*参考文档*

1. VS Code[文档](https://code.visualstudio.com/docs/python/python-tutorial)
![2](https://github.com/hyqing/athena/raw/master/image/set%20workspace.png)
