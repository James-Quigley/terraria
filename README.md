# Terraria

Docker images to run a Terraria Server. Images with [TShock Server](https://tshock.co) or [Vanilla Server](https://terraria.gamepedia.com/Server) are available.

[![](https://images.microbadger.com/badges/image/beardedio/terraria:latest.svg)](https://microbadger.com/images/beardedio/terraria:latest)[![Docker Pulls](https://img.shields.io/docker/pulls/beardedio/terraria.svg)]()[![Docker Stars](https://img.shields.io/docker/stars/beardedio/terraria.svg)]()

### Usage
```
docker create -it \
  --name=terraria \
  -v <path to data>:/config \
  -e world=<world_file_name> \
  -p 7777:7777 \
  beardedio/terraria
```

### Supported tags and respective `Dockerfile` links
* vanilla-1.3.5.3, vanilla-latest [(vanilla/1.3.5.3/Dockerfile)](https://github.com/beardedio/terraria/blob/master/vanilla/1.3.5.3/Dockerfile)
* vanilla-1.3.4.4 [(vanilla/1.3.4.4/Dockerfile)](https://github.com/beardedio/terraria/blob/master/vanilla/1.3.4.4/Dockerfile)
* vanilla-1.3.3.3 [(vanilla/1.3.3.3/Dockerfile)](https://github.com/beardedio/terraria/blob/master/vanilla/1.3.3.3/Dockerfile)
* vanilla-1.3.2.1 [(vanilla/1.3.2.1/Dockerfile)](https://github.com/beardedio/terraria/blob/master/vanilla/1.3.2.1/Dockerfile)
* vanilla-1.3.1.1 [(vanilla/1.3.1.1/Dockerfile)](https://github.com/beardedio/terraria/blob/master/vanilla/1.3.1.1/Dockerfile)
* tshock-4.3.25, tshock-latest, latest [(tshock/4.3.25/Dockerfile)](https://github.com/beardedio/terraria/blob/master/tshock/4.3.25/Dockerfile)
* tshock-4.3.24 [(tshock/4.3.24/Dockerfile)](https://github.com/beardedio/terraria/blob/master/tshock/4.3.24/Dockerfile)
* tshock-4.3.23 [(tshock/4.3.23/Dockerfile)](https://github.com/beardedio/terraria/blob/master/tshock/4.3.23/Dockerfile)
* tshock-4.3.22 [(tshock/4.3.22/Dockerfile)](https://github.com/beardedio/terraria/blob/master/tshock/4.3.22/Dockerfile)
* tshock-4.3.20 [(tshock/4.3.20/Dockerfile)](https://github.com/beardedio/terraria/blob/master/tshock/4.3.20/Dockerfile)
* tshock-4.3.19 [(tshock/4.3.19/Dockerfile)](https://github.com/beardedio/terraria/blob/master/tshock/4.3.19/Dockerfile)
* tshock-4.3.18 [(tshock/4.3.18/Dockerfile)](https://github.com/beardedio/terraria/blob/master/tshock/4.3.18/Dockerfile)
* tshock-4.3.17 [(tshock/4.3.17/Dockerfile)](https://github.com/beardedio/terraria/blob/master/tshock/4.3.17/Dockerfile)
* tshock-4.3.16 [(tshock/4.3.16/Dockerfile)](https://github.com/beardedio/terraria/blob/master/tshock/4.3.16/Dockerfile)
* tshock-4.3.15 [(tshock/4.3.15/Dockerfile)](https://github.com/beardedio/terraria/blob/master/tshock/4.3.15/Dockerfile)
* tshock-dev-2265, tshock-dev-latest [(tshock-dev/2265/Dockerfile)](https://github.com/beardedio/terraria/blob/master/tshock-dev/2265/Dockerfile)
* tshock-dev-2261 [(tshock-dev/2261/Dockerfile)](https://github.com/beardedio/terraria/blob/master/tshock-dev/2261/Dockerfile)
* tshock-dev-2260 [(tshock-dev/2260/Dockerfile)](https://github.com/beardedio/terraria/blob/master/tshock-dev/2260/Dockerfile)
* tshock-dev-2257 [(tshock-dev/2257/Dockerfile)](https://github.com/beardedio/terraria/blob/master/tshock-dev/2257/Dockerfile)
* tshock-dev-2252 [(tshock-dev/2252/Dockerfile)](https://github.com/beardedio/terraria/blob/master/tshock-dev/2252/Dockerfile)
* tshock-dev-2233 [(tshock-dev/2233/Dockerfile)](https://github.com/beardedio/terraria/blob/master/tshock-dev/2233/Dockerfile)
* tshock-dev-2228 [(tshock-dev/2228/Dockerfile)](https://github.com/beardedio/terraria/blob/master/tshock-dev/2228/Dockerfile)
* tshock-dev-2226 [(tshock-dev/2226/Dockerfile)](https://github.com/beardedio/terraria/blob/master/tshock-dev/2226/Dockerfile)
* tshock-dev-2220 [(tshock-dev/2220/Dockerfile)](https://github.com/beardedio/terraria/blob/master/tshock-dev/2220/Dockerfile)
* tshock-dev-2216 [(tshock-dev/2216/Dockerfile)](https://github.com/beardedio/terraria/blob/master/tshock-dev/2216/Dockerfile)

### Quick reference
- Where to get help:
the [TShock Forums](https://tshock.co/xf/index.php?forums/) or the [Terraria Forum](https://forums.terraria.org)

- Where to file issues:
https://github.com/beardedio/terraria/issues

- Maintained by:
[Brandon Skrtich of Bearded.io](https://www.bearded.io/#footer)

- Supported Docker versions:
[the latest release](https://github.com/docker/docker-ce/releases/latest) (down to 1.8 on a best-effort basis)

### What is Terraria Server?
A Terraria server provides a platform for players to connect over the internet or other network for multiplayer games of [Terraria](https://terraria.org/).

## How to use

### Generating a new world
To run with out user intervention Terraria Server needs to be configure to use an already generated world. This means you can use one that you have already generated or you can generate one via docker by running this command:
```
sudo docker run -it -p 7777:7777 \
    -v $HOME/terraria/config:/config \
    --name=terraria \
    beardedio/terraria
```
You can then follow the prompts to create a new world.

### Starting your server with a preexisting world
The world file needs to exist in the config folder.
To start a server using an already generated world, use this command:
```
sudo docker run -dit \
  --name=terraria \
  -v $HOME/terraria/config:/config \
  -e world=<world_file_name> \
  -p 7777:7777 \
  beardedio/terraria
```

If you get an error from docker saying the container name already exists, it means you need to remove your old docker container process.
`sudo docker rm terraria`

If you want to reattach to any running containers:
`sudo docker attach terraria`
Now you can execute any commands to the terraria server. Ctrl-p Ctrl-q will detatch you from the process.

### beardedio/terraria:tshock-<version>
TShock is a server modification for Terraria, written in C#, and based upon the Terraria Server API. It uses JSON for configuration management, and offers several features not present in the Terraria Server normally.

### beardedio/terraria:tshock-dev-<version>
TShock dev are unreleased development builds of TShock. These builds may be unstable but they are updated faster then the released versions so they support new versions of Terraria faster.

### beardedio/terraria:vanilla-<version>
Vanilla Terraria server is the server software provided by the developers of Terraria. This version has only basic features but it is updated along with the main game so it should always be up to date.

If a docker image isn't available of the latest versions please [contact us](https://www.bearded.io/#footer) about the new release so we can update this repo.

### FAQ
- Can I manage my own plugins for tshock?
Yes, if you want manage you own plugins for tshock containers, you can add a volume mount to your docker command via `-v <path to plugins folder>:/tshock/ServerPlugins`. If you want to maintain any of the plugins that ship with tshock, you will need to copy them into the ServerPlugins folder. Mounting the plugins folder will override the plugins that ship with tshock.

#### *Notes*
* Please check the [TShock instructions](https://tshock.atlassian.net/wiki/display/TSHOCKPLUGINS/Configuration+File+Docs) for properly installing and configuring your terraria server.
* Any [additional command-line instructions](https://tshock.atlassian.net/wiki/display/TSHOCKPLUGINS/Command+Line+Parameters) can be added to the end of either method for launching a server.  Docker maps the $HOME/terraria/world linux-host folder to the /tshock/world container-folder.
* More information about running a server is available in the [wiki](https://terraria.gamepedia.com/Server).

#### License

The MIT License (MIT)
Copyright (c) 2018 Brandon Skrtich
