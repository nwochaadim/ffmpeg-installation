# FFMPEG installation on Mac OS

### Steps:
* Install Homebrew:  
```
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```  

* Install FFMPEG dependencies:
```
brew install automake fdk-aac git lame libass libtool libvorbis libvpx opus sdl shtool texi2html theora wget x264 xvid yasm
```

* Clone the ffmpeg repository from github to a folder named ffmpeg on local machine:
```
git clone http://source.ffmpeg.org/git/ffmpeg.git ffmpeg
```  

* Navigate to the folder:

```
cd ffmpeg
```

* Compile and install the libraries:
```
./configure  --prefix=/usr/local --enable-gpl --enable-nonfree --enable-libass --enable-libfdk-aac --enable-libfreetype --enable-libmp3lame --enable-libopus --enable-libtheora --enable-libvorbis --enable-libvpx --enable-libx264 --enable-libxvid
make && sudo make install
```

* Verify Installation:
```
ffmpeg -version
```
If you are able to see the ffmpeg version displayed, means you did everything correctly.
