# ImageHostingService
use to save gif, avoid github issues convert gif to png

```shell

% ffmpeg -v warning -ss 45 -t 2 -i big_buck_bunny_1080p_h264.mov -vf scale=300:-1 -gifflags -transdiff -y bbb-notrans.gif
% ffmpeg -v warning -ss 45 -t 2 -i big_buck_bunny_1080p_h264.mov -vf scale=300:-1 -gifflags +transdiff -y bbb-trans.gif
% ls -l bbb-*.gif
-rw-r--r-- 1 ux ux 1.1M Mar 15 22:50 bbb-notrans.gif
-rw-r--r-- 1 ux ux 369K Mar 15 22:50 bbb-trans.gif


ffmpeg -y -i file.mp4 -vf palettegen palette.png
ffmpeg -y -i file.mp4 -i palette.png -filter_complex paletteuse -r 10 -s 320x480 file.gif
```
