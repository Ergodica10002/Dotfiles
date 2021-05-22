# Dotfiles

Here is some files for setting the environment of a new computer.
Install power

## Vim
The `.vimrc` file helps to set the coding environment of VIM.

## Zsh
The `.zshrc` file helps to set the zsh environment of ZSH.
It is assumed that the [oh-my-zsh](https://github.com/ohmyzsh/ohmyzsh) is also installed.
### Installing Zsh
Install
```bash
sudo apt update
sudo apt install zsh
```
Check now-available shells
```bash
cat /etc/shells
```
Change current shell to zsh
```
chsh -s $(/usr/bin/zsh)
```
### Installing oh-my-zsh
wget
```bash
sh -c "$(wget -O- https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```
curl
```bash
$ sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```
*Note: This runs the `install.sh` in oh-my-zsh. Check all the details in [oh-my-zsh](https://github.com/ohmyzsh/ohmyzsh)*

### Windows
Some features in a theme may not be able to appear correctly in Windows. This uses theme `awesomepanda`, which can work correctly in Windows.
