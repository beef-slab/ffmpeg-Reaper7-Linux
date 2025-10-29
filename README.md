# ffmpeg-Reaper7-Linux
A ffmpeg library that will add ffmpeg to Reaper 7 if you are using a Debian based OS like Debian, Ubuntu, or Mint.

Installation Steps:
1.  Backup your reaper stuff, I'm not a software engineer, I used ChatGPT to make this.
2.  Extract the .so files and paste them into the reaper directory with the executable, mine is in ~/opt/REAPER on Linux Mint.
3.  Launch reaper with the following command after you fill in your file paths: LD_LIBRARY_PATH="/path/to/reaper/directory:$LD_LIBRARY_PATH" /path/to/reaper/executable
4.  You can add the command from step 3 into a script that lanches Reaper with ffmpeg everytime. For my setup I have the Reaper .desktop file point to a script that launches Reaper       with ffmpeg and some Pipewire JACK compatibility stuff. Make sure you add "export" if you make a script so it would look like:                                                         export LD_LIBRARY_PATH="/path/to/reaper/directory:$LD_LIBRARY_PATH" /path/to/reaper/executable

If you get a black screen when trying to play video change your video output setting to RGB instead of OpenGL. This setting is in options, preferences, media, video.

Ffmpeg License Stuff:

This FFmpeg build was compiled from FFmpeg 4.4 with the following configuration:
--prefix=~/ffmpeg4
--enable-gpl --enable-nonfree --enable-shared
--disable-asm
--enable-libx264 --enable-libx265 --enable-libvpx
--enable-libfdk-aac --enable-libmp3lame
--enable-libopus --enable-libvorbis --enable-libass

Source available at: https://ffmpeg.org/releases/ffmpeg-4.4.tar.bz2
