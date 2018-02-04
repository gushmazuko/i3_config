# i3_config
## Install i3wm
```bash
apt update
apt install -s i3 i3blocks fonts-font-awesome
```
## Install i3-gaps
**Dependencies for Debian Stretch**
```bash
apt install libxcb-keysyms1-dev libpango1.0-dev libxcb-util0-dev xcb libxcb1-dev libxcb-icccm4-dev libyajl-dev libev-dev libxcb-xkb-dev libxcb-cursor-dev libxkbcommon-dev libxcb-xinerama0-dev libxkbcommon-x11-dev libstartup-notification0-dev libxcb-randr0-dev libxcb-xrm0 libxcb-xrm-dev
```
Fore more visite [here](https://github.com/Airblader/i3/wiki/Compiling-&-Installing)

**Install i3-gaps**
```bash
cd /opt

# clone the repository
git clone https://www.github.com/Airblader/i3 i3-gaps
cd i3-gaps

# compile & install
autoreconf --force --install
rm -rf build/
mkdir -p build && cd build/

# Disabling sanitizers is important for release versions!
# The prefix and sysconfdir are, obviously, dependent on the distribution.
../configure --prefix=/usr --sysconfdir=/etc --disable-sanitizers
make
sudo make install
```

## Copy configurations
```bash
cd
apt install feh compton
git clone https://github.com/gushmazuko/i3_config.git
cp -r i3_config/.config/i3/ ~/.config/
cp -r i3_config/etc/ /
```
