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

6. Setup Wild Cherry Colours
```
https://github.com/mashaal/wild-cherry

iTerm2 Preferences -> Profiles -> Colors tab -> Color presets
-> Import -> wild-cherry.itermcolors
```

7. Set theme to wild cherry
```
vim ./zshrc
ZSH_THEME="wild-cherry"
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
-> Melso LG M DZ for Powerline
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

## Visual Studio Code Setup

Download from: [Microsoft](https://visualstudio.microsoft.com/downloads/)

List of plugins to install:
```
Atom One Dark
```

Then utilize `cmd+p` to activate all the plugins

### Applications
1. Download `Magnet` from the app store to organize workspaces with shortcuts
2. Download `Snap` from app store, add command ` to open finder
3. Download `Karabiner elements` download vim arrow key complex modification [here](https://pqrs.org/osx/karabiner/complex_modifications/#vi_mode_arrow)

## Files

| File | Description |
| --- | --- |
| `.vimrc` | Configs for `vim` |
| `.zshrc` | Congigs for `zsh` |
