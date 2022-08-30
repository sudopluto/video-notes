source video: https://youtu.be/Bcb3gIjyKg0

- 1: setup rpmfusion, update distro & firmware, install codecs
    - do inital setup, select additional repos if want
    - install rpmfusion: https://rpmfusion.org/Configuration
        - wget https://mirrors.rpmfusion.org/free/fedora/rpmfusion-free-release-36.noarch.rpm
        - wget https://mirrors.rpmfusion.org/nonfree/fedora/rpmfusion-nonfree-release-36.noarch.rpm
        - sudo dnf in *.rpm
    - update distro & install codecs
        - sudo dnf up && sudo dnf groupinstall "Fedora Workstation"
        - video on the groupinstall command: https://youtu.be/TelA7_zzY_M
    - update firmware
        - sudo fwupdmgr update
    - reboot!

- 2: install drivers (nvidia only folks)
    - nvidia drivers video: https://youtu.be/_SIIMhvLP8Y
        - https://rpmfusion.org/Howto/NVIDIA
        - sudo dnf install akmod-nvidia xorg-x11-drv-nvidia-cuda xorg-x11-drv-nvidia-cuda-libs\
            xorg-x11-drv-nvidia-power vdpauinfo libva-vdpau-driver libva-utils
        - sudo grubby --update-kernel=ALL --args='nvidia.NVreg_PreserveVideoMemoryAllocations=1'
        - sudo systemctl enable nvidia-{suspend,resume,hibernate}
    - optional, displaylink driver: https://github.com/displaylink-rpm/displaylink-rpm/releases
    - optional, nvidia firefox hw accel video: https://youtu.be/dCXck6De4sY
        - https://github.com/elFarto/nvidia-vaapi-driver

- 3: setup firefox
    - sign in
    - about:config -> media.ffmpeg.vaapi.enabled -> toggle to true
        - then restart browser
        - video guide: https://youtu.be/dCXck6De4sY
    - set fonts to cantarell
    - set new tab in home to about:newtab
    - install 1080p netflix and ublock orgin addons (if you haven't already)

- 4: setup gnome
    - install steam first, pulls in the libappindicator addon
        - or can just manually install add-on
    - optional: install yaru theme
        - sudo dnf in yaru-theme
    - install gnome tweaks and extentions
        - sudo dnf in gnome-tweaks gnome-extensions-app
    - relog into gnome / reboot
    - setup tweaks and extensions
        - set gnome theme (i like yaru)
        - make mouse accel flat
        - add weekday and secs to top bar
        - add minimize and maximize to window titlebars
        - disable background logo extension
        - enable appindicator extension
    - go through gnome settings app and change stuff
        - night light is cool 
        - dark theme and backgrounds
        - disable shell search
        - setup touchpad
        - set auto timezone and am/pm
        - profile pic
        - computer hostname
    - reboot

- 5: gnome terminal
    - click profile, create a new default profile
    - increase font size
    - use gogh to theme if you want
        - https://gogh-co.github.io/Gogh/
        - bash -c  "$(wget -qO- https://git.io/vQgMr)" 
        - i use clone of ubuntu for the whole ubuntu theme

- 6: any desktop / terminal software
    - install flathub
        - flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo
    - google chrome
        - sudo dnf in google-chrome-stable
    - steam
        - sudo dnf in steam
    - mpv
        - sudo dnf in mpv
    - neovim
        - sudo dnf in neovim
    - for other stuff, experiment with gnome software, try flatpaks first
        - shotcut, gimp, sound recorder, obs, discord

- 7: config files / secret keys
    - secrect keys (like ssh of gpg)
        - have a encrypted usb where i store them
        - copy over and import
            - ssh example: just copy over into ~/.ssh and run $ssh-add
    - config
        - best to have a git repo you can clone / wget from
            - here's mine: https://github.com/sudopluto/config/tree/master/common
        - just wget files into proper locations
        - must haves
            - vimrc / init.vim
            - bashrc
            - mpv config
            - git config
            - vscode config
        - consider a manager like stash if you have a tiling window manager / tmux / other intense setup

- 8: missing dev libraries
    - just google / dnf se a lot to find the package names and reinstall
    - rbenv is your friend for ruby
    - vulkan guide is pretty straight forwards

- 9: setup disks
    - everything you could want can be done from gnome disks now
