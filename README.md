# AI-Writer

原仓库地址: <https://github.com/BlinkDL/AI-Writer>

这是一个 AI 续写文本的项目，该项目被用来为 [electron-mailer2](https://github.com/shampoo6/electron-mailer2) 提供邮件续写功能

## 安装

```shell
# 此处以cpu安装为例
# 其余安装方式可查看原仓库

# 确定 python 版本为 3.7.9 可用
# 原仓库推荐 python 3.8
# 运行以下命令安装 torch
pip install torch
```

然后设置 `run.py` 中的 `RUN_DEVICE` 为 `cpu`

## 运行

```shell
# content(必填): 续写的开头部分
# length: 续写的长度
python run.py <content> [length]
```

> 运行结果我已经使用 `base64` 进行编码，并输出到终端

## 使用 pyinstaller 打包成二进制

安装 pyinstaller

```shell
pip install pyinstaller
```

打包 `run.py`

```shell
pyinstaller run.py
```

输出结果是个 `run.exe` 的可执行程序

输出结果将不包含 `model` 文件夹，所以需要从项目目录下拷贝 `model` 文件夹到输出的 `dist/run` 文件夹中
