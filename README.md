# Build Instructions:
**Note: The following dependency install command is only for users of *Arch Linux* or *Arch Linux-based distributions*.**
**For other Linux distributions, the command and package names will be change.**

## Install Build Dependencies:
```sh
sudo pacman -S glib2 dtc pixman \
zlib ninja libaio \
bluez-libs capstone brltty \
bzip2 libcap-ng libcurl-gnutls \
gtk3 libjpeg-turbo ncurses \
numactl libsasl sdl2 \
libseccomp snappy libssh \
libusb vte3 lzo \
valgrind libnfs libiscsi \
binwalk p7zip qemu-tools \
android-tools base-devel libepoxy \
libdrm mesa libx11 \
virglrenderer libpulse qemu-full \
spice spice-gtk spice-vdagent
```

## Build Commands:
```sh
git clone https://github.com/enamulhasanabid/qemu_a8664.git

cd qemu_a8664 && mkdir build && cd build

../configure \
--enable-sdl \
--enable-opengl \
--enable-virglrenderer \
--enable-system \
--enable-modules \
--audio-drv-list=pa \
--target-list=x86_64-softmmu \
--enable-kvm \
--enable-gtk \
--enable-tools \
--enable-libusb \
--enable-usb-redir \
--enable-spice \
--enable-spice-protocol \
--enable-guest-agent \
--prefix=<FULL_PATH_OF_YOUR_DESIRED_DIRECTORY>

make install -j$(nproc)
```

# See Also:
- https://gitlab.com/qemu-project/qemu
- https://github.com/royalgraphx/SideswipeOnQEMU
- https://github.com/royalgraphx/qemu-sideswipe/tree/wx86_64

# Credits:
- Special thanks to *@knxwille* for beta testing and support
