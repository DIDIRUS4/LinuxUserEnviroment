# Linux User Enviroment
- Useful commands and packages for make your life easier in Linux

### Useful Packages/Cmds
- Installing CloudFlare Warp-Client from AUR
> 1. Install `cloudflare-warp-bin`
> 2. Open terminal
> 3. Write in terminal: `sudo systemctl enable warp-svc.service && sudo systemctl start warp-svc.service && sudo systemctl status warp-svc.service` ![Screenshot_20220404_162441](https://user-images.githubusercontent.com/77334306/161553603-87824823-4b8d-4f26-8655-feea67978f60.png)
> 4. Great! Try it for yourself `warp-cli --help` (For example, let's try connect via WARP+DOH (Translate: Proxy tunnel + 1.1.1.1 DNS CF Servers)
> Write this commands `warp-cli set-mode warp+doh && warp-cli -l connect && warp-cli network` Enjoy! Another Information search in `warp-cli --help`


# ManjaroLifeHacks
This is not Manjaro software, just some tweaks to make your life easier


# Manjaro GNU Linux - Switching via prime
> 1. Open Terminal (Konsole Manjaro or another GNU Linux System with Nvidia-prime)
> 2. Go to path of your program
> 3. For me it's MultiMC Launcher `cd ~/.local/share/multimc && prime-run sh MultiMC`
> 4. Enjoy! You run MultiMC Launcher and other MultiMC trees with Nvidia GPU Priority (Now MultiMC still use Nvidia, not amd/intel graphics)

### Negative factors

- The system does not use your graphics card to its full potential, so sometimes even the integrated graphics will be better.

# Manjaro KDE Approved Bug | Error while change user avatar (icon)

- If you try change user avatar in Manjaro KDE you'll get a error

### Easy F I X
> 1. Open Manjaro Settings Manager ![Screenshot_20220227_104857](https://user-images.githubusercontent.com/77334306/155873505-b2aaa230-eff5-48dd-a161-1723f2f8de64.png)
> 
> 2. Go to "User Accounts" ![Screenshot_20220227_105040](https://user-images.githubusercontent.com/77334306/155873560-6e9956cb-f518-4f76-b8a5-179908ecf748.png)
 
> 3. Click on your account ![Screenshot_20220227_105101](https://user-images.githubusercontent.com/77334306/155873573-b94094c8-ee2c-4264-90f3-c6248cae1eaf.png)

> 4. Click on your avatar and select picture

# Installing MultiMC Minecraft Instance Launcher for Manjaro GNU/LINUX

> 1. mkdir multimc-pkgbuild
> 2. cd multimc-pkgbuild
> 3. wget https://raw.githubusercontent.com/MultiMC/multimc-pkgbuild/master/PKGBUILD
> 4. makepkg -si
> 5. Press `Meta` button (like Microsoft Windows button) and type `Multimc` in search area

# Manjaro Plasma Rare Bug | Mouse freezed at one position X,Y on monitor and doesn't react
### ~~Easy fix (Works 9 times out of 10)~~ Fixed in latest Manjaro Releases
> ~~1. Press `L.CTRL` button + `F1 --> F2` buttons~~
> ~~1.1 If `1` point doesn't work, try push `ESCAPE/CTRL/ENTER` buttons~~
> ~~2. Enjoy!~~

# [KDE Connect](https://kdeconnect.kde.org/) ~~FIX~~ allow input/output connection with UFW
> 1. Open your Terminal (bash, zsh)
> 2. Insert command line `sudo ufw allow 1714:1764/udp && sudo ufw allow 1714:1764/tcp`
> 3. Enjoy!

# Fix Noto Sans Emoji on Arch based distributions
> 1. For example incorrect view emoji in Discord Application. Open terminal as sudo.
> 2. `sudo pacman -S noto-fonts-emoji`
> 3. `sudo fc-cache -fv` or `reboot` your linux system.
> 4. Enjoy with fixed emojiiiiii ^u^

# Fix Bluetooth audio in Minecraft on Linux (Ubuntu/Arch)
> 1. Open Terminal
> 2. 2.0 For Ubuntu: `sudo vim /etc/openal/alsoft.conf` 
> 3. 2.1 For Arch: `sudo vim /etc/xdg/alsoft.conf`
> 4. Find `# drivers =` and replace with `drivers = alsa` in 2.1 point you need to create alsoft.conf and write `drivers = alsa`
> 5. It works fine on Pop! Os (Based on Ubuntu) and Arch based System like Endeavour OS. It's should be works on any Ubuntu/Arch based systems.