# Dotfiles

Here are some files for setting the environment of a new computer.

If any error messaage comes like `Not an editor command: ^M`, use vim to open file and set the format correctly by `:set fileformat=unix`.

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
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```
*Note: This runs the `install.sh` in oh-my-zsh. Check all the details in [oh-my-zsh](https://github.com/ohmyzsh/ohmyzsh)*

### Installing the Powerline fonts
Some themes needs the [Powerline fonts](https://github.com/powerline/fonts) to appear correctly.
```bash
sudo apt-get install fonts-powerline
```

### Ubuntu
This uses theme `agnoster`. I made some changes from default version. See `./Zsh/Ubuntu/agnoster.zsh-theme`
* Add current time in RPROMPT
* Remove the machine name in PROMPT

Copy the `.zsh-theme` file to `~/.oh-my-zsh/themes/`

The terminal looks like this:
<div align=center>
<img src=/Zsh/Ubuntu/Ubuntu_agnoster.png width=640 height=360 />
</div>

### Windows
Some features in a theme may not be able to appear correctly in Windows. This uses theme `awesomepanda`, which can work correctly in Windows. I made some changes from default version. See `.Zsh/Windows/awesomepanda.zsh-theme`
* Add current time in RPROMPT
* Remove the machine name in PROMPT

Copy the `.zsh-theme` file to `~/.oh-my-zsh/themes/`

The terminal looks like this:
<div align=center>
<img src=/Zsh/Windows/Windows_terminal_awesomepanda.png width=640 height=360 />
</div>

## GitBash
`GitBash` is a tool in [Git for Windows](https://gitforwindows.org/). It provides a simple way to use git with Bash environment in Windows besides wsl.

Install Git for Windows and one can see GitBash in the `Start Menu`

The followig was referenced from [this](https://juejin.cn/post/6844903700775845895).
### git-prompt.sh
It is used for me to define the prompt($PS1) in `GitBash`. Copy it into the `/etc/profile.d` directory.
```bash
cp git-prompt.sh /etc/profile.d/git-prompt.sh
```
Compared with default, I delete the host machine name and add the current time. The prompt looks like this:
<div align=center>
<img src=/GitBash/GitBash_prompt.png width=640/>
</div>

### .bash_profile
It is used for me to add user-defined aliases. Copy it into the home directory in GitBash. 
```bash
cp .bash_profile ~/.bash_profile
```
