# Setting-up-terminal-and-text-editor
The following steps taken from igor boguslavsky [video](https://youtu.be/pk3H6gOCalk) 
# Setting up zsh

```bash
chsh -s /usr/bin/zsh    #then reboot the computer or Log Out then Log In. 
```

After rebooting the terminal will ask you if you want to configure it in any specific way. Just type 0.

```bash
0        #just type 0
```

# Installing fzf 
a very handy tool that make the history of your commands so much easier to access.

```bash
git clone --depth 1 https://github.com/junegunn/fzf.git ~/.fzf  # Downloading fzf

```

```bash
~/.fzf/install       # Calling the installation script
```
# Installing antigen for zsh on Ubuntu

```bash
curl -L git.io/antigen > .antigen.zsh
```
# Templet Configuration

```bash
nano .zshrc  # Remove first 2 lines
```
Copy the content of this file and put it inside .zshrc

```bash

# Init antigen.
source "$HOME/.antigen.zsh"

# Configure antigen.
antigen use oh-my-zsh

# Plugins
antigen bundle git
antigen bundle command-not-found
antigen bundle zsh-users/zsh-completions
antigen bundle zsh-users/zsh-syntax-highlighting
antigen bundle srijanshetty/zsh-pip-completion
antigen bundle MichaelAquilina/zsh-auto-notify
antigen bundle unixorn/autoupdate-antigen.zshplugin
antigen bundle iboyperson/pipenv-zsh
antigen bundle trystan2k/zsh-tab-title
antigen bundle zpm-zsh/undollar
antigen bundle mafredri/zsh-async

# Set theme
antigen theme subnixr/minimal

# Apply antigen settings.
antigen apply

# Use Python 3 by default.
alias python=python3
alias pip=pip3

# Use the fzf by default
[ -f ~/.fzf.zsh ] && source ~/.fzf.zsh
```
Once you done you need to source your terminal
```bash
source ~/.zshrc
```
# Installing VSCode on Ubuntu
```bash
sudo snap install --classic code  
```
