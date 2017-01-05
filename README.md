# giffer
Easily make gifs from a/b loop points in MPV.

This is a script to easily generate a gif file from the a/b loop points in MPV. I started from the code on http://blog.pkh.me/p/21-high-quality-gif-with-ffmpeg.html and modified it to work better with mpv, as well as have a few minor changes.

Technically, MPV is optional since you can easily use the script by itself in the shell.

# Requirements

- [mpv](https://mpv.io/) (video player; optional)
- ffmpeg (to actually generate the gif)
- bc (to calculate the duration from a/b start/end points; not optional if you want frame precision since bash's built-in `expr` command doesn't support floating point)

# Setup

- Add the line in input.conf to your mpv's input.conf file (usually located at ~/.config/mpv/input.conf; create it if it doesn't exist already)
- Change the paths in that line to point to the location where you put the 'giffer' script, and the location where you want the gif to be saved.

# Usage

- Play a video file using MPV.
- Press `l` to set the start point of the gif.
- Press `l` again to set the end point of the gif.
- After the start and end points have been defined, press `g` to export the gif.
- Press `l` a third time to clear the loop and continue watching the video.
- For extra precision, you can pause the video and then use `.` and `,` to move forward or backward by one frame.
