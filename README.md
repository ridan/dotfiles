# dotfiles
This toolchain uses Dotfiles.

## Setup
You need to have Dotfiles installed on your machine.

### Check if brew exists
If it doesn’t then paste this on the terminal 
(From the home-brew website)
```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

Python already exist on Mac but it’s better to get the one by brew since it has all the tools like pip 

```
brew install python
```

Mac Python is installed on `/usr/bin/python` brew will install python in `usr/local/bin/python`

`export PATH="/usr/local/opt/python/libexec/bin:$PATH"` will allow you use the brew python for the terminal session the zshrc files should take care of that once it's all setup

Now that you have python we can install pip
```
brew install pip
```

Install the dotfiles tool
```
pip install dotfiles
```

### Setup all dotfiles
```
dotfiles —sync
```
This will paste all dotfiles into your homedirectory as a simlink

Check if they exist in the home directory
`ls -a`

## Now install ZSH
from the website (https://github.com/robbyrussell/oh-my-zsh)
```
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```
This should now pick up the `.zshrc` file and load up all your configurations. For some reason it also set the default to zsh which I am not sure how it does that but if you face this issue then you need to fix it

## Configuer VIM
Install vundle the vim plugin manager
```
git clone https://github.com/VundleVim/Vundle.vim.git ~/.vim/bundle/Vundle.vim
```
Go into vim and run `:PluginInstall`

Terminal vars are’t showing up. Need to fix that

## Install nodeJS
Install nodeJS from brew
```
brew install node
```
Install NVM to manage the node versions
```
curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.4/install.sh | bash
```

## Configure Git
```
git config --global user.name "ridan"
```

## Miscellaneous Terminal configs

### Make cursor fast
`System Preferences => Keyboard => Key Repeat Rate`
### Option + left/right moves the cursor back or forward words
`Item -> preference -> keys -> +`

keyboard action: `<option> left`
Action: `send escape sequence` and choose
`b for left and f for right`