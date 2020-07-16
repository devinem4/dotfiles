# dotfiles
Inspired by the [missing semester lecture on vim](https://missing.csail.mit.edu/2020/editors/), using this repo to track my dotfiles and system setup.

### vim
[vim-plug](https://github.com/junegunn/vim-plug)  
`:PlugInstall`

### YouCompleteMe Plugin
https://github.com/ycm-core/YouCompleteMe
1. Install development tools, CMAKE, and python  
`$ sudo apt install build-essential cmake python3-dev`
2. Restart Terminal
3. Install a pre-built vim package with python support built in  
`$ sudo apt install vim-gtk`
4. `$ cd ~/.vim/plugged/YouCompleteMe` 
5. `$ python3 install.py --ts-completer`

### node
```console
$ cd /usr/local/lib
$ sudo mkdir nodejs
$ cd nodejs
$ sudo wget https://nodejs.org/dist/v12.18.2/node-v12.18.2-linux-x64.tar.xz
$ sudo tar -xJvf node-v12.18.2-linux-x64.tar.xz
```

Update `~./profile`
```
# nodejs
VERSION=v12.18.2
DISTRO=linux-x64
export PATH=/usr/local/lib/nodejs/node-$VERSION-$DISTRO/bin:$PATH
export PATH=/home/mddevine/.npm-global/bin:$PATH
```

Refresh profile with `$ . ~./profile`  
Test with `$ node --version`

```
$ node -g install js-beautify
$ js-beautify --version
```
