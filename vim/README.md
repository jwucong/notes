# vim编辑器


### 1. windows10下安装vim
  1. [下载vim压缩包(gvim_8.1.0796_x64.zip)](https://github.com/vim/vim-win32-installer/releases)
  2. 将zip包解压到你想要安装的目录(D:\App\vim)
  3. 将vim.exe所在的目录路径添加到系统环境变量中(D:\App\vim\vim81)

### 2. vim打开文件
```bash
# 快速打开powershell
win+x a

# 打开当前目录下的README.md文件
vim README.md

# 打开当前目录下的多个文件
vim text.txt index.html main.js
```

### 3. vim三种模式
  1. 命令模式(按Esc进入)
  2. 编辑(输入)模式(按i, I, r, R, o, O, a, A, s, S进入对应的编辑模式)
  3. 底线命令模式(输入:+命令执行对应的指令)
  
### 4. vim移动光标
> 有两种移动光标的方式

1. h: 左, j: 下, k: 上, l: 右
2. 使用上下左右方向键

### 5. 常用编辑指令
> 替换时，如果带有指令c, 则会出现如下确认提示"替换为 xxx (y/n/a/q/l/^E/^Y)？", 其中选项：  
  y: 替换当前匹配  
  n: 跳过当前匹配  
  a: 替换全部匹配  
  q: 不替换并退出  
  l: 替换当前匹配并退出(是L键不是i键)  
  ^E: 往下滚动页面  
  ^Y: 网上滚动页面
  
* v 逐字选中，V 逐行选中
* y 复制
* d 剪切
* p 粘贴
* x 删除(删除当前光标所在位置的字符)
* c 修改(删除当前选中区域并进入编辑模式)
* u 撤销
* . 重做
* /string 查找"string"，按n查找下一个，按N查找上一个
* :s/old/new 在当前行使用new替换第一个old(可在后面加其他指令如:s/old/new/igc, i忽略大小写，g整行替换，c替换前需要确认)
* :%s/old/new 在当前文件使用new全局替换old(:%s/old/new/igc, i忽略大小写，g全局替换，c替换前需要确认)