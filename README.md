# rstreams
stream multile youtube videos

If you have a live event that has multiple streams, instead of using
the resources of an entire browser tab per stream and trying to line up
things on your screen, here is an alternative.

List each youtube share url on its own line in a file 'rstreams.list'.

Run 'rstreams' and it will spawn an xterm per video which will then
show output from essentially 'yt-dlp -o - | ffplay -'.

Interacting with ffplay then permits:
```
- resized/relocate as desired
- 'm'          : muted
- 'up arrow'   : speed up video to catch up to realtime
- 'right arrow': skip forward to catch up to realtime
```
amongst other keybindings of ffplay.

If a stream exits prematurely or otherwise has issues, one can launch
just the one stream by specifying the stream number.

```
rstream 2
```

will launch the 3rd video as counting starts at 0.
