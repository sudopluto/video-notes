source video: https://youtu.be/jIbh1_5NPeI

- how is fedora workstation dominating the linux desktop?
    - well its 8+ years of refinement:
    - https://blogs.gnome.org/uraeus/2014/04/16/preparing-the-ground-for-the-fedora-workstation/

- i was still in high school when i first remembered fedora workstation being announced as a project
    - most new distros were skins of ubuntu
    - systemd vs upstart
    - wayland was intangible, mir was still around
    - obs-studio just started development
    - kde neon didn't exist yet

- only 3 big (corperate backed linux distros)
    - fedora & redhat
        - known for being strict with foss and thus rough around edges
    - ubuntu and canonical
        - default desktop distro, most users & user friendly
    - opensuse & suse
        - similar to fedora, but with even less users and less support for 3rd party packages

- so what changed?
    - wayland and the tightening of viable desktop linux
        - only daily driving compositor is gnome
            - kde is on it's way up
            - if you want wayland, you NEED to run gnome
            - this means a lot more focus was put onto gnome, as xfce, lxde, lxqt, etc all fell away
    - flatpak (and it's victory over snaps)
        - ubuntu no longer held onto a monopoly of 3rd party packages
        - PPAs went from convience to cumbersome
        - underlying distro matters less as more and more applications "just werk"
        - ubuntu clinging onto snaps and forcing them onto users only ruins more goodwill
            - ex: calculator, firefox, etc
    - new innovations led by red hat, and debuting in Fedora
        - fwupd
        - wayland & latest gnomes
        - libinput
        - flatpak
        - pipewire and wireplumber
    - codecs, drivers, & font rendering become less of issues
        - openh264, polishing of rpmfusion, flatpaks
        - nvidia drivers getting better under fedora (now plus open source!)
        - glvnd making ubuntu-drivers nvidia prime implemention outdated
    - gaming became a thing
        - fedora includes new kernels and drivers in the updates for their releases
            - this is needed, for gaming periphirals and amdgpus
    - upgrades "just werk"
        - fedora upgrades are some of the most stable, most users are on the couple most recent releases

- all of this is outlined better in Christian Schaller's blog
    - https://blogs.gnome.org/uraeus/2021/09/24/fedora-workstation-our-vision-for-linux-desktop/
    - but general idea is that fedora / redhats policy of upstreaming the contributions allowed
    them to control the future of the linux desktop
        - unlike ubuntu's policy of silo'ing their contribution (ex: ubuntu-drivers)
    - meanwhile, ubuntu has made almost no contributions to the modern linux desktop stack besides
    some optimizations to gnome
        - instead they are using their captive users to dogfood stuff like snaps
