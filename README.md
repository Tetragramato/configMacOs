# Mac OS Configuration for developers

## Brew / Initial configuration

```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
```
- brew cask install iterm2

```
defaults write com.apple.Finder AppleShowAllFiles true
```

## Zsh

```
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

Follow https://gist.github.com/kevin-smets/8568070

- Brew install zsh-syntax-highlighting
- brew install exa
- brew install fd
- brew install rg
- brew install fzf

```
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```

## Usefull/Misc
- brew cask install menumeters
- brew cask install alfred
- brew install jq
- brew install watch
- brew install tree

### Fonts

- brew tap homebrew/cask-fonts
- brew cask install font-hack-nerd-font
- brew cask install font-jetbrainsmono-nerd-font-mono
- brew cask install font-jetbrainsmono-nerd-font

## SDK/Node version management

### Sdkman

```
curl -s "https://get.sdkman.io" | bash
```
- source "$HOME/.sdkman/bin/sdkman-init.sh"
- sdk install java 8.0.242.hs-adpt

### Nvm

```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.2/install.sh | bash
```
- nvm install node

## Development

### Common

- brew cask install docker
- brew cask install atom
- brew cask install intellij-idea
- brew install git
- brew cask install visual-studio-code
- brew cask install slack
- brew cask install zoom
- brew cask install tunnelblick

### Kubernetes

- brew tap dtan4/tools
- brew cask install osxfuse
- brew install datawire/blackbird/telepresence
- brew install kubernetes-cli
- brew install kubectx
- brew install k8sec
- brew install telepresence
- brew install helm
- brew install kind
- brew cask install google-cloud-sdk

### JS

- brew install yarn --ignore-dependencies

## Git configuration

- touch ~/.gitignore_global

```
# OS generated files #
######################
.DS_Store
.DS_Store?
._*
.Spotlight-V100
.Trashes
ehthumbs.db
Thumbs.db
```

- git config --global core.excludesfile ~/.gitignore_global
- git config --global user.name `"toto"`
- git config --global user.email `toto@toto.fr`
- git config --global pull.rebase true
- git config --global core.editor "code --wait"
