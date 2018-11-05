# moos-ivp-nctu-docker
This docker file contains two main repos
* MOOs-IvP - 
* RobotX-2014-MIT

## How to get docker images
There are 2 ways to get docker images

1. build from dockfer file
```
$ docker build -t moos-ivp-nctu -f Dockerfile .
```
2. get docker from docker hub
```
$ docker pull tonycar12002/moos-ivp-nctu
```

## How to run
```
$ xhost +local:root
$ sudo service nvidia-docker start
$ nvidia-docker run -it --rm --env="DISPLAY" --env="QT_X11_NO_MITSHM=1" --volume="/tmp/.X11-unix:/tmp/.X11-unix:rw" moos-ivp-nctu
```

## Test the moos-ivp 
1. Test simple mission
```
container# cd /root/moos-ivp/ivp/missions/s1_alpha
container# ./launch.sh
```
you will see MOOSApp pMarinneViwer pop out and then press button "deploy"


![pMarineviewer](https://github.com/tonycar12002/moos-ivp-nctu-docker/pMarineviewer.png)

</br>
2. Test RobotX 2014 Task1-Qualifying
```
container# cd /root/moos-ivp/robotx-mit-2014/ATTIC/missions_test/Task1
container# ./launch.sh
```
press button "deploy"
![pMarineviewer](https://github.com/tonycar12002/moos-ivp-nctu-docker/Task1.png)