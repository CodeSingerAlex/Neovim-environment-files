# Neovim-environment-files

通过拉取本库可以快速完成neovim的配置，在这之前需要先完成前置配置

## 依赖

### 支持丰富色彩和图标的客户端

1.下载自由度更高色彩支持更好的终端`iTerm2`

https://iterm2.com

2.下载管理zsh配置的开源框架`oh my zsh`

https://github.com/ohmyzsh/ohmyzsh

3.下载zsh主题`powerlevel10k`

https://github.com/romkatv/powerlevel10k

4.配置zsh主题

打开`~/.zshrc`并修改`ZSH_THEME`

```shell
...
ZSH_THEME = "powerlevel10k/powerlevel10k"
...
```

使配置文件生效`source ~/.zshrc`

此时会询问是否下载`Meslo Nerd Font`，输入y下载

重启客户端会出现指引，选择自己喜欢的配置即可

如果想要配置得更美观`cmd + ,`进行个人进行配置

### Nerd Font

我们需要安装一个Nerd Font来确保图标的正确显示。

先执行下面命令使得Homebrew可以安装nerd font：

```
brew tap homebrew/cask-fonts
```

下载一款Nerd Font:

```shell
brew install font-meslo-lg-nerd-font
```

配置到iTerm2

使用`command + 、`打开设置（也可以在顶部iTerm2选项卡选择settings）

选择`profile` -> `Text` -> `Font` -> 下拉找到`MesloLGS Nerd Font Mono`

### 后续插件依赖

```shell
brew install ripgrep
```

安装[ripgrep](https://github.com/BurntSushi/ripgrep)，这是后面安装搜索功能需要的依赖

后面的使用mason安装lsp服务时需要用到npm这里提前配置，下载node会同时安装npm，命令如下：

```shell
brew install node
```

## 下载

下载`neovim`

```shell
brew install neovim
```

拉取本库

```shell
git clone https://github.com/CodeSingerAlex/Neovim-environment-files.git
```

将库中的`nvim`文件夹移动到`~/.config/`

```shell
mv Neovim-environment-files/nvim ~/.config/
```

打开`neovim` `lazy.nvim`会自动加载插件、`mason.nvim`会自动加载`lsp`服务，因为需要一次性载入大量插件，会略有卡顿，确保网络通畅避免自动拉取插件失败。

```shell
nvim
```
