
Build it by

```
$ docker build -t moos-ivp-nctu -f Dockerfile .
```

How to run
```
$ xhost +local:root
$ sudo service nvidia-docker start
$ nvidia-docker run -it --rm --env="DISPLAY" --env="QT_X11_NO_MITSHM=1" --volume="/tmp/.X11-unix:/tmp/.X11-unix:rw" moos-ivp-nctu

```# moos-ivp-nctu-docker
