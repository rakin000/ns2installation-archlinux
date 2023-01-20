# Install ns-2.35 and nam-1.15 on ArchLinux(EndeavourOS) 
## Install gcc-4.8 
- If you don't have 'yay', install it. 
  - Clone [yay](https://aur.archlinux.org/packages/yay)
  ```bash
     git clone https://aur.archlinux.org/yay.git
  ```
  - Change directory and install 
  ```bash 
     cd yay
     makepkg -si
  ```
- Now install gcc-4.8 
  ```bash 
     yay -S gcc48 
  ```
## Download [ns-allinone-2.35_gcc5.tar.gz](https://drive.google.com/file/d/11rYcVLmZw8aF_F0-3uealuScGoO1tWMo/view?usp=sharing)
- Extract and change directory 
  ```bash 
    tar -xf ns-allinone-2.35_gcc5.tar.gz 
    cd ns-allinone-2.35/
  ```
## Install nam-1.15 and ns-2.35
- First install dependencies 
```bash 
   sudo pacman -S libx11 libxmu
```
- To install, run 
```bash 
    export CC=gcc-4.8 CXX=g++-4.8 && ./install 
```
- After this script runs successfully 
  - Change directory to nam-1.15 and install
  ```bash 
     cd nam-1.15/
     sudo make install 
  ```
  - Change directory to ns-2.35 and install 
  ```bash
      cd ../ns-2.35/
      sudo make install
  ```
