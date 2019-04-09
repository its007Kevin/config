# Config

**Config** is a checklist I follow to set up a new Mac's development environment. It gets me up to speed so I can more quickly get back to coding.

## Zsh Setup

1. Install Homebrew
```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
brew --version
```

2. Install iTerm2
```
brew cask install iterm2
```

3. Install zsh
```
brew install zsh
```

4. Install oh-my-zsh
```
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

5. Set zsh as the default terminal environment
```
iTerm2 Preferences -> Profile -> General
-> paste /bin/zsh in the "Command" textbox
and restart iTerm2
```

6. Setup Material Design Colours
```
curl -O https://raw.githubusercontent.com/MartinSeeler/iterm2-material-design/master/material-design-colors.itermcolors

iTerm2 Preferences -> Profiles -> Colors tab -> Color presets
-> Import -> material-design-colors.itermcolors

rm material-design-colors.itermcolors
```

7. Set theme to agnoster
```
vim ./zshrc
ZSH_THEME="agnoster"
```

Set `whoami` to `DEFAULT_USER` to prevent verbose pre-line information `user:host` on local machines. Add the following to the `~/.zshrc`
```
cat .zshrc >> ~/.zshrc
```


1. Install Powerline fonts
```
git clone https://github.com/powerline/fonts.git --depth=1
cd fonts
./install.sh
cd ..
rm -rf fonts
```
```
iTerm2 -> Preferences -> Profile -> Text -> Change Font 
-> Melso LG L DZ for Powerline
```

9. Add the Syntax Highlighting Plugin
```
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting

vim ~/.zshrc
```
Add `plugins = (plugin1 zsh-syntax-highlighting)`
```
source .zshrc
```

10. Add Auto Suggestions Plugin
```
git clone https://github.com/zsh-users/zsh-autosuggestions $ZSH_CUSTOM/plugins/zsh-autosuggestions

vim ~/.zshrc
```
Add `plugins = (plugin1 zsh-autosuggestions)`
```
source .zshrc
```

11. Add Other Useful Plugin
```
docker-compose (provides aliases)
```

12. Copy `.vimrc` into the root directory
```
cat .vimrc >> ~/.vimrc
```

## Visual Studio Code Setup

Download from: [Microsoft](https://visualstudio.microsoft.com/downloads/)

List of plugins to install:
```
Markdown All in One
Material Theme
Material Icon Theme
Python
Visual Studio IntelliCode - Preview
```

Then utilize `cmd+p` to activate all the plugins

## Files

| File | Description |
| --- | --- |
| `.vimrc` | Configs for `vim` |
| `.zshrc` | Congigs for `zsh` |

### Applications
 IDE

### Todo

- Setup a script to get the latest configurations to update the github repository
  - Ex: On change to `.vimrc` run a bash command that will automatically update `.vimrc` in the repo and upload the github
