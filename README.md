# kickstart.nvim

## Installation (MacOS)

```
brew install neovim ripgrep fd
```

## Installation (Ubuntu/Debian)

### Install essential tools

```
sudo apt install make git curl build-essential
```

### Install Neovim
```sh
curl -LO https://github.com/neovim/neovim/releases/latest/download/nvim-linux-x86_64.tar.gz
sudo rm -rf /opt/nvim-linux-x86_64
sudo tar -C /opt -xzf nvim-linux-x86_64.tar.gz
```

Then add this to your shell config (~/.bashrc, ~/.zshrc, ...):

```
export PATH="$PATH:/opt/nvim-linux-x86_64/bin"
```

### Install [ripgrep](https://github.com/BurntSushi/ripgrep#installation)

Check the latest releases here: https://github.com/BurntSushi/ripgrep/releases

```sh
curl -LO https://github.com/BurntSushi/ripgrep/releases/download/15.1.0/ripgrep_15.1.0-1_amd64.deb
sudo dpkg -i ripgrep_15.1.0-1_amd64.deb
```

### Install [fd-find](https://github.com/sharkdp/fd#installation)

Check the latest releases here: https://github.com/sharkdp/fd/releases

```sh
curl -LO https://github.com/sharkdp/fd/releases/download/v10.3.0/fd_10.3.0_amd64.deb
sudo dpkg -i fd_10.3.0_amd64.deb
```


### Install Kickstart

> [!NOTE]
> Backup your previous configuration (if any exists)

Neovim's configurations are located under the following paths, depending on your OS:

| OS | PATH |
| :- | :--- |
| Linux, MacOS | `$XDG_CONFIG_HOME/nvim`, `~/.config/nvim` |
| Windows (cmd)| `%localappdata%\nvim\` |
| Windows (powershell)| `$env:LOCALAPPDATA\nvim\` |


#### Clone kickstart.nvim


##### Linux and Mac

```sh
git clone https://github.com/luyiming/kickstart.nvim.git "${XDG_CONFIG_HOME:-$HOME/.config}"/nvim
```


### Post Installation

Start Neovim

```sh
nvim
```

Wait until all plugins are installed. Type `:Mason`, and install corresponding LSP servers:

- python: install `ruff`, `pyright`
- rust: install `rust_analyzer`

### Uninstall

See [lazy.nvim uninstall](https://lazy.folke.io/usage#-uninstalling) information

