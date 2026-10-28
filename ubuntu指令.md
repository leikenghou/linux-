# 省略sudo密碼
vim /etc/sudoers
ben 	ALL=(ALL:ALL) NOPASSWD:ALL

# 安裝zsh與oh my zsh
sudo apt update && sudo apt install zsh -y
https://ohmyz.sh/#install

# oh my zsh 插件
plugins=(git
	 zsh-autosuggestions
	 zsh-syntax-highlighting
	 z
	 extract
	)

# 安裝DRACULA_THEME
git clone https://github.com/dracula/zsh.git
DRACULA_THEME="$PWD/zsh"
cp -r "$DRACULA_THEME/dracula.zsh-theme" "$DRACULA_THEME/lib" "${ZSH:-$HOME/.oh-my-zsh}/themes/"

Open ~/.zshrc and set:
ZSH_THEME="dracula"
source ~/.zshrc

# dock欄美化
sudo apt install gnome-shell-extension-manager
# 安裝blur my shell 與 dash in panel
