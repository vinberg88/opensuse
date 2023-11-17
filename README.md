# Opensuse - Tumbelweed - WSL - KDE - Plasma!

How to install KDE plasma Opensuse Tumbelweed - Windows 11 - WSL2

1. Install OpenSuse Tumbelweed

2. Config GWSL and reboot

3. Start Tumbelweed from GWSL

4. Add systemd (if nano not works. Install it: sudo zypper in nano)

Type in terminal: sudo nano /etc/wsl.conf

Copy to terminal and save:

[boot]
systemd=true

5. Reboot

6. Update Tumbelweed in terminal: sudo zypper ref -b && sudo zypper dup

7. Install this programs - good =)

sudo zypper install bash git npm wget curl nano sudo dialog go dracut opi

sudo zypper ar -cfp 90 https://ftp.gwdg.de/pub/linux/misc/packman/suse/openSUSE_Tumbleweed/ packman
sudo zypper dup --from packman --allow-vendor-change  <-- press a in terminal

opi codecs

8. Install this: sudo zypper in -t pattern wsl_gui wsl_base wsl_systemd

9. Time to install kde: sudo zypper install -t pattern kde kde_plasma

10 Type - sudo yast and update all and install xorg

11. Paste in terminal: xdg-user-dirs-update

12. Paste in terminal: sudo systemctl set-default multi-user.target

13. Paste in terminal: sudo systemctl set-default graphical.target

14 In terminal type: sudo nano ~/.bash_ubuntu_desktop

Paste this in terminal and save:

# Vinberg - Fyren 1488
# Start to flight adolf!
# --------------------
# Setting up essential environment variables
# --------------------

export XDG_CURRENT_DESKTOP=ubuntu:GNOME
export XDG_SESSION_DESKTOP=ubuntu
export DESKTOP_SESSION=ubuntu
export GNOME_SHELL_SESSION_MODE=ubuntu

# Commonly referenced environment variables for X11 sessions
# https://specifications.freedesktop.org/basedir-spec/latest/

export XDG_CONFIG_DIRS=/etc/xdg/xdg-ubuntu:/etc/xdg
export XDG_DATA_DIRS=/usr/share/ubuntu:/usr/local/share:/usr/share:/var/lib/snapd/desktop
export XDG_MENU_PREFIX=gnome-

export XDG_SESSION_TYPE=x11
export XDG_SESSION_CLASS=user
export GDK_BACKEND=x11

# Disables using Direct3D in Mesa 3D graphics library
export LIBGL_ALWAYS_SOFTWARE=1

15. Reboot

16. Paste in terminal: . ~/.bash_ubuntu_desktop

17. Type in terminal: dbus-launch startplasma-x11
