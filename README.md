# work-environment
My Kali workspace.
## REQUIREMENTS
- Kali, or debian derived.

## PREVIEW
<img src='assets/preview_01.png'>
<img src='assets/preview_02.png'>

## STEPS

```sh
sudo apt update
sudo apt upgrade
sudo apt update
sudo apt install build-essential git vim xcb libxcb-util0-dev libxcb-ewmh-dev libxcb-randr0-dev libxcb-icccm4-dev libxcb-keysyms1-dev libxcb-xinerama0-dev libasound2-dev libxcb-xtest0-dev libxcb-shape0-dev -y
cd ~Descargas
git clone https://github.com/baskerville/bspwm.git
git clone https://github.com/baskerville/sxhkd.git
cd bspwm/
make
sudo make install
cd ../sxhkd/
make
sudo make install
 
sudo apt install bspwm -y

mkdir ~/.config/bspwm
mkdir ~/.config/sxhkd
cd ~/Descargas/bspwm/
cp examples/bspwmrc ~/.config/bspwm/
chmod +x ~/.config/bspwm/bspwmrc 
cp examples/sxhkdrc ~/.config/sxhkd/
```

#### REPLACE '~/.config/sxhkd/sxhkdrx' content with 'github:sxhkd/sxhkdrc' content
#### REPLACE '~/.config/bspwm/scripts/bspwm_resize' content with 'github:bspwm/scripts/bspwm_resize' content
#### REPLACE '~/.config/bspwm/bspwmrc' content with 'github:bspwm/bspwmrc' content

```sh
sudo apt install cmake cmake-data pkg-config python3-sphinx libcairo2-dev libxcb1-dev libxcb-util0-dev libxcb-randr0-dev libxcb-composite0-dev python3-xcbgen xcb-proto libxcb-image0-dev libxcb-ewmh-dev libxcb-icccm4-dev libxcb-xkb-dev libxcb-xrm-dev libxcb-cursor-dev libasound2-dev libpulse-dev libjsoncpp-dev libmpdclient-dev libcurl4-openssl-dev libnl-genl-3-dev -y

cd ~/Descargas/
git clone --recursive https://github.com/polybar/polybar
cd polybar/
mkdir build
cd build/
cmake ..
make -j$(nproc)
sudo make install

sudo apt update
sudo apt install meson libxext-dev libxcb1-dev libxcb-damage0-dev libxcb-xfixes0-dev libxcb-shape0-dev libxcb-render-util0-dev libxcb-render0-dev libxcb-randr0-dev libxcb-composite0-dev libxcb-image0-dev libxcb-present-dev libxcb-xinerama0-dev libpixman-1-dev libdbus-1-dev libconfig-dev libgl1-mesa-dev libpcre2-dev libevdev-dev uthash-dev libev-dev libx11-xcb-dev libxcb-glx0-dev -y

cd ~/Descargas
git clone https://github.com/ibhagwan/picom.git
cd picom/
git submodule update --init --recursive
meson --buildtype=release . build
ninja -C build
sudo ninja -C build install

sudo apt install rofi -y
```

#### REBOOT AND OPEN SESSION WITH BSWPWM WORKSPACE

```sh
sudo apt install firejail -y

cd /usr/local/share/fonts
sudo wget https://github.com/ryanoasis/nerd-fonts/releases/download/v2.1.0/Hack.zip
sudo unzip Hack.zip
fc-cache -v

sudo apt install feh

cd ~/Imágenes
wget https://raw.githubusercontent.com/Sonkoh/workspace/assets/wallpaper.png

mkdir ~/.config/polybar
cd ~/Descargas
git clone https://github.com/adi1090x/polybar-themes.git
bash polybar-themes/setup.sh
```

#### SELECT 1

```sh
git clone https://github.com/Sonkoh/workspace.git
rm -r ~/.config/polybar/hack
cp -r workspace/polybar ~/.config/polybar
mkdir ~/.config/picom
cp workspace/picom.conf ~/.config/picom/picom.conf
sudo apt install neofetch alsa-utils xclip scrot -y
sudo su root
cd ~
wget https://github.com

git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ~/powerlevel10k
echo 'source ~/powerlevel10k/powerlevel10k.zsh-theme' >>~/.zshrc
zsh
sudo su 
cd ~
wget https://github.com/sonkoh/workspace/argon.tar.gz
tar -xzvf argon.tar.gz  
bash argon/install.sh -i -b Grey
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ~/powerlevel10k
echo 'source ~/powerlevel10k/powerlevel10k.zsh-theme' >>~/.zshrc
zsh
```
### 'Neofetch', 'Oh My Tmux', 'Bat', 'LSD'
