# Tmux

[Tmux](https://github.com/tmux/tmux)是一个终端复用软件，它可以让你在单一屏幕上创建和使用多个终端。它最大的作用是可以让你的终端会话永不掉线！

## 原理

通过伪终端技术来实现，类似相关的应用有`SSH`、`Telnet`

> 相关介绍:  
> [伪终端原理](https://www.cnblogs.com/zzdyyy/p/7538077.html)

## 使用

### 启动

`.bash_aliases`中设置别名
```
alias tmux='tmux -2'
```

这样启动的`Tmux`会支持256色

### 配置文件

系统配置文件路径`/etc/tmux.conf`，用户配置文件路径`~/.tmux.conf`

另外，`Tmux`支持插件，对应有插件管理应用[TPM](https://github.com/tmux-plugins/tpm)

[配置备份](github地址)


### 配置说明

1. 键位映射
```
bind-key -T root C-p send-keys Up
```

将`Ctrl-p`映射为`Up`键， `-T root`表示键位映射记入到`root`表中，这样`Ctrl-p`就直接映射为`Up`键了，不需要前置键来解析。

2. 选项设置
```
set -g option 
```

### 常用操作

1. `tmux new-session -s session_name` 创建新的session
2. `tmux attach-session -t session_name` 重连已经存在的某个session
3. `man tmux` 查看`Tmux`帮助文档
