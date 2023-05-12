# To get the files in working condition
Type the following into your bash shell one at a time
``` bash
echo ".cfg" >> .gitignore
git clone --bare <remote-git-repo-url> $HOME/.cfg
alias config='/usr/bin/git --git-dir=$HOME/.cfg/ --work-tree=$HOME'
config config --local status.showUntrackedFiles no
config checkout
```
# Neovim
# Tmux
# Bash



# Other notes:
### To create another like this one
The following is when you want to create another repository like this
```bash 
git init --bare $HOME/.cfg
alias config='/usr/bin/git --git-dir=$HOME/.cfg/ --work-tree=$HOME'
echo "alias config='/usr/bin/git --git-dir=$HOME/.cfg/ --work-tree=$HOME'" >> $HOME/.zsh/aliases
config config --local status.showUntrackedFiles no
config add .vimrc + config commit -m "add .vimrc"
```
