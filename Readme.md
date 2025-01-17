[![wakatime](https://wakatime.com/badge/user/49ee5b93-5588-4f44-a2a6-bceec1836f4a/project/11927978-fe31-424f-8dc8-e6278c354e31.svg)](https://wakatime.com/badge/user/49ee5b93-5588-4f44-a2a6-bceec1836f4a/project/11927978-fe31-424f-8dc8-e6278c354e31) [![Docker Image CI](https://github.com/JonasFranke/DockerDiscordStatusBot/actions/workflows/docker-build.yml/badge.svg)](https://github.com/JonasFranke/DockerDiscordStatusBot/actions/workflows/docker-build.yml) ![Libraries.io dependency status for GitHub repo](https://img.shields.io/librariesio/github/JonasFranke/DockerDiscordStatusBot) [![CodeFactor](https://www.codefactor.io/repository/github/jonasfranke/dockerdiscordstatusbot/badge)](https://www.codefactor.io/repository/github/jonasfranke/dockerdiscordstatusbot)
[![FOSSA Status](https://app.fossa.com/api/projects/git%2Bgithub.com%2FJonasFranke%2FDockerDiscordStatusBot.svg?type=shield)](https://app.fossa.com/projects/git%2Bgithub.com%2FJonasFranke%2FDockerDiscordStatusBot?ref=badge_shield)

# ⚠️ DISCLAIMER: Mounting the docker socket into the container is a security risk. If you don't know what you are doing, don't do it. ⚠️
Mounting the docker socket into a container gives that container full access to the Docker daemon and its capabilities. This includes the ability to run any other containers or images, access the network, and access any host file system that is mapped into the container. Essentially, it allows the container to have complete control over the host system. This can be a serious security risk if the container is compromised or if an attacker is able to gain access to the container.
# DockerDiscordStatusBot
A simple Discord bot that allows you to see the status of any docker container.
View the DockerHub page [here](https://hub.docker.com/r/jnsfrnk/ddsb).

---
### How to use
- Clone the repository
- Build a jar using ```gradle shadowJar```
- Build a docker image using ```docker build -t <image name> .```
- Run the docker image using ```docker run -v //var/run/docker.sock:/var/run/docker.sock --network=host --name ddsb -e DISCORD_TOKEN=<YOUR-DISCORD-BOT-TOKEN> <image name>```

#### Using the pre-built image:
- Clone the image from DockerHub using ```docker pull jnsfrnk/ddsb:latest```
- Run the docker image using ```docker run -v //var/run/docker.sock:/var/run/docker.sock --network=host --name ddsb -e DISCORD_TOKEN=<YOUR-DISCORD-BOT-TOKEN> jnsfrnk/ddsb:latest```

- Add the bot to your server
- Use the ```/ds``` command to see all running containers
- Use the ```/stopupdating <TRUE/FALSE>``` command to stop the bot from updating the status



## License
[![FOSSA Status](https://app.fossa.com/api/projects/git%2Bgithub.com%2FJonasFranke%2FDockerDiscordStatusBot.svg?type=large)](https://app.fossa.com/projects/git%2Bgithub.com%2FJonasFranke%2FDockerDiscordStatusBot?ref=badge_large)