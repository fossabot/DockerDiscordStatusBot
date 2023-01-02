[![wakatime](https://wakatime.com/badge/user/49ee5b93-5588-4f44-a2a6-bceec1836f4a/project/11927978-fe31-424f-8dc8-e6278c354e31.svg)](https://wakatime.com/badge/user/49ee5b93-5588-4f44-a2a6-bceec1836f4a/project/11927978-fe31-424f-8dc8-e6278c354e31)
# DockerDiscordStatusBot
A simple Discord bot that allows you to see the status of any docker container.

---
### How to use
- Clone the repository
- Build a jar using ```gradle shadowJar```
- Build a docker image using ```docker build -t <image name> .```
- Run the docker image using ```docker run -v //var/run/docker.sock:/var/run/docker.sock --network=host --name ddsb <image name>```

- Add the bot to your server
- Use the ```/ds``` command to see all running containers
- Use the ```/stopupdating <TRUE/FALSE>``` command to stop the bot from updating the status

