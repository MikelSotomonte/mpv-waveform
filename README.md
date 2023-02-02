# mpv-waveform
This [mpv](https://mpv.io/) script displays [ffmpeg video waveforms](https://trac.ffmpeg.org/wiki/WaveformMonitor) in realtime
It's based on [this mpv histogram script](https://github.com/detuur/mpv-scripts)

This script does *not* support config files,
because of the nested options. Please edit the options
in the `opts` array in the script itself.  

There are three default keybinds:
 - `c`: Toggle the waveform on/off
 - `C` (`Shift+c`): Cycle between the waveform formats available
 - `Alt+c`: Toggle the waveform's location, between top and bottom

These keybinds can be changed by placing the following lines
in your `input.conf`:
```
KEY script-binding toggle-waveform
KEY script-binding cycle-waveform-type
KEY script-binding toggle-waveform-position
```
### A note on hardware decoding
The histogram filter is not compatible with hardware decoding. As a result, the
default behaviour is to automatically disable any hardware decoding while the
filter is on. This behaviour can be changed in the aforementioned `opts` array.
![Screenshot - video: Sprite Fright Blender Open Movie](https://cdn.discordapp.com/attachments/446054699439882250/1001900605557710888/mpv-shot0002.jpg)

![Screenshot - video: Sprite Fright Blender Open Movie](https://cdn.discordapp.com/attachments/446054699439882250/1001908424646344764/mpv-shot0004.jpg)
