# Setting Up Hyper Terminal and OhMyZsh with Powerlevel10k Theme

![image](https://github.com/ACHUX21/Hyper-dotfiles/assets/130113878/6e92c766-5359-4ddf-bc69-71557a444cb7)




**Step 1: Install Hyper Terminal**
Download the Hyper Terminal package using the following link: [Hyper Terminal Download](https://releases.hyper.is/download/deb) && dpkg -i hyper.deb
##
**Step 2: Configure Hyper Terminal**
Run the following commands to set up the Hyper Terminal configuration and background image:
```bash
curl -s https://raw.githubusercontent.com/ACHUX21/config-dotfiles/main/.hyper.js |sed "s|/home/achux21|$(echo $HOME)|g" > ~/.hyper.js
curl https://wallha.com/download/ws/14/z84ATcoI-wallha.com.png > ~/Pictures/term.png
```
Pictures: [Wallha.com](https://wallha.com/tag/selective-coloring/2)
##
**Step 3: Set Zsh as the Default Shell and Install OhMyZsh**
Install Zsh, set it as the default shell, and install OhMyZsh by executing the following commands:
```bash
sudo apt install zsh
chsh -s $(which zsh)
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
exec zsh
```
##
**Step 4: Set Fonts For Icons...**
```bash
mkdir -p ~/.local/share/fonts/
wget -O ~/.local/share/fonts/Hasklig.zip https://github.com/ryanoasis/nerd-fonts/releases/download/v3.1.1/Hasklig.zip
unzip ~/.local/share/fonts/Hasklig.zip -d ~/.local/share/fonts/
```
##
**Step 5: Configuring powerlevel10k**
```bash
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ~/powerlevel10k
echo 'source ~/powerlevel10k/powerlevel10k.zsh-theme' >>~/.zshrc
source ~/.zshrc
```
**Step 6: Install Exa**
```bash
sudo apt install exa
echo -e "alias ls='exa --icons --color=always --group-directories-first'\nalias ll='exa -alF --icons --color=always --group-directories-first'\nalias la='exa -a --icons --color=always --group-directories-first'\nalias l='exa -F --icons --color=always --group-directories-first'" >> ~/.zshrc
source ~/.zshrc
```

# That's It

![giphy](https://github.com/ACHUX21/Hyper-dotfiles/assets/130113878/38c90cf9-0244-4632-985f-24e20ffb2b59)

