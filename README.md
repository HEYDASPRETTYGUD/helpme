# helpme
This is fine.
./configure --enable-cuda --enable-cuvid --enable-nvenc --enable-libnpp --enable-nonfree --prefix=/usr --extra-version=0ubuntu0.22.04.1 --toolchain=hardened --libdir=/usr/lib/x86_64-linux-gnu --incdir=/usr/include/x86_64-linux-gnu --arch=amd64 --enable-gpl --disable-stripping --enable-gnutls --enable-ladspa --enable-libaom --enable-libass --enable-libbluray --enable-libbs2b --enable-libcaca --enable-libcodec2 --enable-libdav1d --enable-libfontconfig --enable-libfreetype --enable-libfribidi --enable-libgme --enable-libgsm --enable-libjack --enable-libmp3lame --enable-libmysofa --enable-libopenjpeg --enable-libopenmpt --enable-libopus --enable-libpulse --enable-librabbitmq --enable-librubberband --enable-libshine --enable-libsnappy --enable-libsoxr --enable-libspeex --enable-libssh --enable-libtheora --enable-libtwolame --enable-libvidstab --enable-libvorbis --enable-libvpx --enable-libwebp --enable-libx265 --enable-libxml2 --enable-libxvid --enable-libzimg --enable-libzmq --enable-libzvbi --enable-lv2 --enable-omx --enable-openal --enable-opencl --enable-opengl --enable-sdl2 --enable-pocketsphinx --enable-librsvg --enable-libvpl --enable-libdc1394 --enable-libdrm --enable-libiec61883 --enable-chromaprint --enable-frei0r --enable-libx264 --enable-shared 


sudo apt install \
  build-essential yasm cmake pkg-config \
  libfreetype6-dev libx264-dev libx265-dev libnuma-dev \
  libnpp-dev nvidia-cuda-toolkit nvidia-cuda-dev \
  libvpx-dev libfdk-aac-dev libmp3lame-dev libopus-dev \
  libass-dev libfontconfig1-dev


sudo find / -name cdio.pc 2>/dev/null

export PKG_CONFIG_PATH=/usr/lib/x86_64-linux-gnu/pkgconfig:$PKG_CONFIG_PATH

ubuntu@ubuntu-Precision-5540:~/ffmpeg$ nano Makefile 
ubuntu@ubuntu-Precision-5540:~/ffmpeg$ make -j$(nproc)
Makefile:1: *** Too many open files.  Stop.
ubuntu@ubuntu-Precision-5540:~/ffmpeg$ sudo apt install libfreetype6-dev
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
Note, selecting 'libfreetype-dev' instead of 'libfreetype6-dev'
libfreetype-dev is already the newest version (2.13.2+dfsg-1build3).
The following packages were automatically installed and are no longer required:
  nvidia-firmware-550-550.120 python3-netifaces
Use 'sudo apt autoremove' to remove them.
0 upgraded, 0 newly installed, 0 to remove and 8 not upgraded.
ubuntu@ubuntu-Precision-5540:~/ffmpeg$ make distclean
Makefile:1: *** Too many open files.  Stop.
ubuntu@ubuntu-Precision-5540:~/ffmpeg$ rm Makefile 
ubuntu@ubuntu-Precision-5540:~/ffmpeg$ make distclean
make: *** No rule to make target 'distclean'.  Stop.
