# Elementary XP
Desde que eu fui forçado a migrar do Deepin por causa do suporte ao HW do meu note novo eu voltei a olhar pro Elementary que eu sempre quis usar...



## Isso funciona para o video
https://connorkuehl.github.io/dell-inspiron-7559-linux-guide/ 
https://www.reddit.com/r/linux_gaming/comments/aoh5be/guide_hybrid_graphics_on_linux_nvidia_optimus/?utm_source=amp&utm_medium=&utm_content=post_body \
https://gist.github.com/wangruohui/df039f0dc434d6486f5d4d098aa52d07 \
https://community.clearlinux.org/t/bash-scripts-to-automate-installation-of-nvidia-proprietary-driver/368 \
https://www.reddit.com/r/linux_gaming/comments/aoh5be/guide_hybrid_graphics_on_linux_nvidia_optimus/ \
https://forum.manjaro.org/t/howto-set-up-prime-with-nvidia-proprietary-driver/40225 \
https://ricostacruz.com/til/fractional-scaling-on-xorg-linux (escala do video igual ao ubuntu) \
https://gist.github.com/Brainiarc7/aa43570f512906e882ad6cdd835efe57 (tuning da placa intel)

Referencias:

Dell:
https://www.dell.com/support/article/br/pt/brbsdt1/sln298431/um-guia-para-a-nvidia-optimus-em-pcs-dell-com-um-sistema-operacional-ubuntu?lang=pt \

Blacklist nouveau \
https://linuxconfig.org/how-to-disable-nouveau-nvidia-driver-on-ubuntu-18-04-bionic-beaver-linux \
https://tutorials.technology/tutorials/85-How-to-remove-Nouveau-kernel-driver-Nvidia-install-error.html \
http://lxle.net/forums/discussion/1457/tutorial-how-to-blacklist-nouveau-install-nvidia-drivers/p1

A propria nvidia falar pra usar o driver da distro
https://www.nvidia.com.br/Download/driverResults.aspx/156799/br \
http://us.download.nvidia.com/XFree86/Linux-x86_64/435.21/README/index.html


touch blacklist-nouveau-nvidia.conf \
nano blacklist-nouveau-nvidia.conf \
blacklist nouveau \
blacklist lbm-nouveau \
options nouveau modeset=0 \
alias nouveau off \
alias lbm-nouveau off

echo options nouveau modeset=0 | sudo tee -a /etc/modprobe.d/balcklist-nouveau-kms.conf

sudo update-initramfs -u \
reboot

sudo apt install nvidia-driver-XXX nvidia-prime nvidia-settings




## GTK

gsettings set org.gnome.desktop.interface gtk-theme Ant \
gsettings set org.gnome.desktop.wm.preferences theme Ant

https://github.com/snwh/paper-gtk-theme

https://github.com/numixproject/numix-gtk-theme

https://github.com/B00merang-Project
https://github.com/B00merang-Project/Windows-10 \

https://github.com/nana-4/materia-theme \

https://github.com/adapta-project/adapta-gtk-theme \

https://github.com/pop-os/gtk-theme \

https://github.com/arc-design/arc-theme

https://github.com/EliverLara/Ant-Dracula

https://github.com/EliverLara/Nordic

## Icons
Vince
https://github.com/vinceliuice/Tela-icon-theme \
https://github.com/vinceliuice/Tela-circle-icon-theme \
https://github.com/vinceliuice/Qogir-icon-theme \
https://github.com/vinceliuice/emerald-icon-theme

Numix
https://github.com/numixproject/numix-icon-theme \
https://github.com/numixproject/numix-icon-theme-square \
https://github.com/numixproject/numix-icon-theme-circle

Papirus
https://github.com/PapirusDevelopmentTeam/papirus-icon-theme

Sam Hewitt
https://github.com/snwh/paper-icon-theme \
https://github.com/snwh/suru-icon-theme

La Capitaine
https://github.com/keeferrourke/la-capitaine-icon-theme

Ubuntosh Icons
https://github.com/USBA/Ubuntosh-Icons

Ubuntu
https://github.com/ubuntu/yaru

Boston
https://github.com/heychrisd/Boston-Icons

daniruiz
https://github.com/daniruiz/flat-remix

Elementary
https://github.com/elementary/icons

Deepin
https://github.com/linuxdeepin/deepin-icon-theme

PopOS
https://github.com/pop-os/icon-theme


## tema de cursor
https://www.gnome-look.org/p/1084938/ \
https://github.com/ganwell/dmz-cursors hdpi \
https://code.launchpad.net/ubuntu/+source/dmz-cursor-theme \
https://github.com/madsrh/yet-another-DMZ-cursor-theme \
https://github.com/KDE/breeze/tree/master/cursors \



## gtk titulos
https://github.com/sprite-1/elementary-patches/tree/master/design/smaller_titlebar_for_non-gtk_applications



## Sinapse e indicadores
https://github.com/mdh34/elementary-indicators \
https://itsfoss.com/best-indicator-applets-ubuntu/

https://www.youtube.com/watch?v=rg2YBhl7Zhg synapse \
http://www.webupd8.org/2013/06/synapse-indicator-new-search.html \
https://app.simplenote.com/p/tJ0t2R

https://elementaryos.stackexchange.com/questions/13058/replacing-slingshot

https://www.reddit.com/r/elementaryos/comments/fbkp2n/elementary_os_hera_51_app_window_switcher_custom/


## Perfect elementary references
https://gist.github.com/ezeeyahoo/b21c0e12bf4c39622af8 \
http://eos-snippets.blogspot.com/2014/02/add-open-as-root-to-pantheon-files.html \
https://gist.github.com/ankurk91/2327d4881d71a098e3bfcd0b1c255d83 \
https://ditchwindows.com/elementary-os-community-tips-and-tricks/ \
https://averagelinuxuser.com/after-install-elementary-juno/ \
https://gist.github.com/Surendrajat/418d5fd66876848a7f21870fe09365a7 \
https://www.saminiir.com/configuring-arch-linux-on-dell-xps-15/



## single click (no need sudo)
gsettings set io.elementary.files.preferences single-click false


## default wallpaper + lidghtdm 


------------------

## etc/systemd to reduce timeout for shutdown
https://unix.stackexchange.com/questions/273876/a-stop-job-is-running-for-session-c2-of-user \
Disable "Continue running background apps when Google Chrome is closed". \
https://github.com/systemd/systemd/issues/1615#issuecomment-203507283 \
https://unix.stackexchange.com/questions/328317/reducing-shutdown-timeout-for-a-stop-job-is-running \
https://askubuntu.com/questions/800479/ubuntu-16-04-slow-boot-apt-daily-service \

https://elementaryos.stackexchange.com/questions/12155/desktop-takes-forever-to-load-after-restart

## Flicker free booting improvments
Systemd Alinhando XDG_VTNR \
https://unix.stackexchange.com/questions/521037/what-is-the-environment-variable-xdg-vtnr \ https://askubuntu.com/questions/910108/why-is-my-gdm-at-a-different-tty-than-my-desktop-environment \
https://unix.stackexchange.com/questions/399986/systemd-change-default-login-tty

/etc/init/lightdm.conf \
/etc/systemd/system/display-manager.service

## agetty remove blinking cursor
https://wiki.archlinux.org/index.php/Silent_boot \
http://eos-snippets.blogspot.com/2013/10/fix-boot-screen-plymouth-after.html \

## TLP no PopOS
https://support.system76.com/articles/battery/ \
https://www.linuxbabe.com/linux-server/how-to-enable-etcrc-local-with-systemd
https://github.com/pop-os/system76-power

## Performance
https://4fasters.com.br/2018/08/14/tunando-seu-sistema-linux-com-tuned/ \
https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/6/html/power_management_guide/tuned \
https://wiki.debian.org/BootProcessSpeedup \
https://konkor.github.io/cpufreq/about/ \
https://www.youtube.com/watch?v=3JRaQ-MxwV8 \
http://www.brendangregg.com/linuxperf.html \
https://github.com/brendangregg/perf-tools

https://wiki.archlinux.org/index.php/Improving_performance \
https://www.akitaonrails.com/2017/01/17/optimizing-linux-for-slow-computers

Hibernate
https://elementaryos.stackexchange.com/questions/8927/how-to-enable-hibernate-option-in-menu-loki



## drivers
https://unix.stackexchange.com/questions/41817/linux-how-to-find-the-device-driver-used-for-a-device/225496#225496

## SSD
https://easylinuxtipsproject.blogspot.com/p/ssd.html \
https://medium.com/@dardovaldez/fine-tunning-a-ssd-for-a-t470-ubuntu-18-04-b504dceaef50 \
https://www.addictivetips.com/ubuntu-linux-tips/best-ssd-friendly-file-systems-on-linux/ \
https://wiki.debian.org/SSDOptimization \
https://wiki.archlinux.org/index.php/Solid_state_drive \
https://askubuntu.com/questions/792814/how-to-check-if-my-ubuntu-is-placed-on-ssd \
https://www.tecmint.com/find-linux-filesystem-type/ \
https://wiki.archlinux.org/index.php/E4rat

## gestures
https://www.youtube.com/watch?v=ArBCfhVsTZw \
https://support.apple.com/pt-br/HT204895 \
https://www.windowscentral.com/windows-10-touchpad-gestures \
https://www.tenforums.com/tutorials/148114-how-enable-disable-touchpad-multifinger-gestures-windows-10-a.html

## APT
 sudo add-apt-repository -y ppa:apt-fast/stable
 sudo apt -y install apt-fast
 echo "alias apt='apt-fast'" >> ~/.bashrc 
 source ~/.bashrc
https://qastack.com.br/ubuntu/319433/making-mirror-mirrors-ubuntu-com-highly-available \
https://vitux.com/how-to-speed-up-package-downloads-and-updates-with-apt-fast-on-ubuntu/ \
https://github.com/jblakeman/apt-select/blob/master/README.rst \
https://github.com/ilikenwf/apt-fast \
https://itsfoss.com/apt-vs-apt-get-difference/ \
https://www.ostechnix.com/how-to-find-and-remove-unused-packages-in-linux/ \
https://www.hiroom2.com/2016/05/18/ubuntu-16-04-auto-apt-update-and-apt-upgrade/ \
https://debian-handbook.info/browse/stable/sect.regular-upgrades.html

## Plank settings
https://www.linuxuprising.com/2019/12/a-guide-to-using-plank-dock-on-linux.html

## topbar
https://www.omgubuntu.co.uk/2017/04/change-gnome-shell-font \
https://www.fossmint.com/topicons-plus-display-gnome-icons-in-the-top-panel/ \
https://unix.stackexchange.com/questions/276951/how-to-change-the-titlebar-height-in-standard-gtk-apps-and-those-with-headerbars \
https://elementaryos.stackexchange.com/questions/6840/how-to-replace-wingpanels-applications-text-with-a-icon-in-freya

https://github.com/donadigo/wingpanel-indicator-namarupa
https://forum.elementarybr.org/d/36-como-usar-os-aplicativos-que-dependem-dos-indicadores-no-juno/8



## tiling window
https://github.com/microsoft/PowerToys
https://www.linuxuprising.com/2019/07/material-shell-is-new-tiling-shell-for.html
https://www.youtube.com/watch?v=NrG594GvS8k

https://www.youtube.com/watch?v=fjdonz3_Z-I
https://spin.atomicobject.com/2018/07/12/tiling-window-managers-macos/
https://github.com/ianyh/Amethyst
youtube.com/watch?v=J8ywPXvL03A


## editor markdown
https://github.com/lainsce/quilter

## terminal themes
http://mayccoll.github.io/Gogh/

## gnome session cache
https://wiki.archlinux.org/index.php/GNOME/Tips_and_tricks

## Fonts
http://www.linuxfromscratch.org/blfs/view/svn/x/tuning-fontconfig.html
https://www.fossmint.com/fontbase-font-manager-for-linux-designers/
https://www.reddit.com/r/archlinux/comments/5r5ep8/make_your_arch_fonts_beautiful_easily/
https://forums.linuxmint.com/viewtopic.php?t=286734
common way
sudo apt-get install –reinstall ttf-mscorefonts-installer
sharing windows folder
https://www.ostechnix.com/install-microsoft-windows-fonts-ubuntu-16-04/
https://en.wikibooks.org/wiki/Category:Book:Guide_to_X11
https://www.linux.com/tutorials/how-change-your-linux-console-fonts/
https://www.extron.com/article/videowallfontsize
http://resources.printhandbook.com/pages/viewing-distance-font-size.php
https://alexandre.deverteuil.net/docs/archlinux-consolefonts/
https://wiki.archlinux.org/index.php/Microsoft_fonts
xdpyinfo | grep resolution
https://wiki.archlinux.org/index.php/Xorg
https://www.w7df.com/p/windows-10.html


## privacy/ security
https://github.com/hectorm/hblock
https://github.com/pi-hole/pi-hole
https://linoxide.com/linux-how-to/chomper-command-line-tool-block-website-linux/
https://github.com/SecUpwN/Spotify-AdKiller
https://itsfoss.com/set-up-firewall-gufw/
https://wiki.ubuntu.com/UncomplicatedFirewall
https://www.msp360.com/resources/blog/ubuntu-security-hardening-best-practices/
http://www.yolinux.com/TUTORIALS/LinuxTutorialInternetSecurity.html


## Gala
https://www.youtube.com/watch?v=-_JQG7Q7MtE

## Sound
https://www.reddit.com/r/elementaryos/comments/8epuj9/jack_and_pulse_and_making_music_with_loki/
https://github.com/christophgysin/pasystray
https://www.youtube.com/watch?v=lC6GHtLnoKE
player
https://github.com/artemanufrij/playmymusic
sound themes
https://github.com/linuxdeepin/developer-center/issues/1004
https://askubuntu.com/questions/1154064/add-sound-theme-to-18-04
https://opensource.com/article/18/6/sound-themes-linux
https://elementaryos.stackexchange.com/questions/2593/how-do-you-change-the-alert-sound
https://elementaryos.stackexchange.com/questions/17040/how-can-i-disable-sound-effect-of-deleting-files-in-elementary-os-5
https://www.debugpoint.com/2018/08/how-install-sound-themes-ubuntu-linux/
https://sites.google.com/site/xiangyangsite/home/technical-tips/linux-unix/ubuntu/cusomize-sound-theme-for-ubuntu



## greeter
https://www.reddit.com/r/elementaryos/comments/d3mxfi/change_new_greeters_background/
https://github.com/elementary/greeter/tree/blurred-background

https://www.faqforge.com/linux/set-lightdm-wallpaper-that-is-independant-of-the-users-wallpaper-ubuntulinux-mint/
gsettings get org.gnome.desktop.background picture-uri


## Download tools
https://persepolisdm.github.io/
transmission

## Wireless
https://diolinux.com.br/2019/01/como-resolver-o-problema-wireless-realtek-rtl8723be-ubuntu-linux-mint.html
https://bbs.deepin.org/archiver/?tid-150451.html
https://itsfoss.com/speed-up-slow-wifi-connection-ubuntu/
https://www.reddit.com/r/elementaryos/comments/1y2y6u/no_wireless_connections_found_on_elementaryos/
https://medium.com/@surajmandal/using-old-mintdrivers-in-elementary-os-to-fix-driver-issues-working-2017-4b858f00157d

## Zram
https://github.com/GalliumOS/zram-config

## Accounts + ControlCenter
https://www.reallinuxuser.com/how-to-add-more-online-accounts-to-elementary-os-by-installing-gnome-control-center/

## Tilling windows
https://ssokolow.com/quicktile/

## LibreOffice
https://www.libreoffice.org/download/download/
https://wiki.documentfoundation.org/Documentation/Install/Linux#Debian_.2F_Ubuntu_.2F_Mint
https://documentation.libreoffice.org/en/english-documentation/
https://github.com/heychrisd/Boston-Icons


