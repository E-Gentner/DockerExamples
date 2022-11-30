### Heimdall Container

The Heimdall container is an easy way to group all containers that have a web ui together.
It gives you an easy access, customizeable UI that lets you generate buttons that open the ui in a new window
I find it very useful for accessing different containers without having to remember the port and when you don't need all the tools of other containers like portainer or other management containers
&nbsp;
&nbsp;
&nbsp;
/n
### Using docker CLI to run the container
docker run -d \
  --name=heimdall \
  -e PUID=1000 \
  -e PGID=1000 \
  -e TZ=America/New_York \
  -p 80:80 \
  -v /home/pibox/DockerExamples/configs/heimdall/config:/config \
  --restart unless-stopped \
  lscr.io/linuxserver/heimdall:latest


