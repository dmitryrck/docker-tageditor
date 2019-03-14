# EasyTag and Picard

EasyTag and Picard using docker.

## Running

```shell
$ docker run --rm \
  -e DISPLAY=unix:0 \
  -e GDK_DPI_SCALE \
  -e GDK_SCALE \
  -v /etc/localtime:/etc/localtime:ro \
  -v /tmp/.X11-unix:/tmp/.X11-unix \
  -u $(id -u) \
  -e HOME \
  -v $HOME/Books:$HOME/Books \
  -v $HOME/Dropbox/Calibre-config:$HOME/.config/calibre \
  dmitryrck/tageditor easytag
```

Or use [x11docker](https://github.com/mviereck/x11docker):

```terminal
$ x11docker dmitryrck/tageditor easytag
```
