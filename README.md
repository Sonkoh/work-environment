# work-environment
My Kali work environment.
### STEPS

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
