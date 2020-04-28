# WhatToDoAfterGettingANewMac
Notes to record what to do after getting a new macbook.

### Setup
1. iTerm
[Download](https://www.iterm2.com/) & install.

2. zsh
```sh
# install
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"

### zsh-autosuggestions ###
# clone the repository
git clone https://github.com/zsh-users/zsh-autosuggestions ~/.zsh/zsh-autosuggestions

# add to the ~/.zshrc
source ~/.zsh/zsh-autosuggestions/zsh-autosuggestions.zsh

# make it work
source ~/.zshrc

### zsh-synax-highlighting ###
# clone the resposity
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ~/.oh-my-zsh/plugins/zsh-syntax-highlighting

# add to plugins in .zshrc
plugins=( [plugins...] zsh-syntax-highlighting)

# make it work
source ~/.zshrc

### history & z plugins ###
# add to plugins in .zshrc
plugins=( [plugins...] history z)

# make it work
source ~/.zshrc
```

3. ShadowSocksR
> I don't know.

4. Homebrew
[Install](https://brew.sh/)

5. ProxyChains
```sh
# install proxychains4
brew install proxychains-ng

# check the port that socks5 use in ~/.ShadowsocksX-NG/gfwlist.js
# check the head of the file

# add config to proxychains4
vi /usr/local/etc/proxychains.conf

# add the follow line to the end of the file
# and remember to comment out the socks4 config
socks5  127.0.0.1 1086 # the port that shadowsocks use, based on the shadowsocks in your computer

# usage
# add proxychains4 before the command you type
proxychains4 git clone ...

```

Add alias:
```sh
# add to ~/.zshrc
alias pc='proxychains4'

# make it work
source ~/.zshrc
```

6. nvm
```sh
brew install nvm
```

7. node
```sh
# install
nvm install node

# use
nvm use node
```

8. yarn
```sh
brew install yarn
```

9. VSCode
[Download](https://code.visualstudio.com/) & install.

10. SSH Key
```sh
# create folder
mkdir .ssh

# generate key pair
cd ~/.ssh
ssh-keygen -t rsa -C "youremail@email.com"

# use the public key
cd ~/.ssh
cat id_rsa.pub
```
