### Allowing experimental on Docker server
# faced this issue when I tryied to build squash docker image.

```bash
vim /etc/docker/daemon.json
```
and then add this code:
```
{
	"experimental": true
}
```
now, restart the docker service 
```
sudo systemctl restart docker
```

Last but not least 
check the docker 
```
docker version -f '{{.Server.Experimental}}'
```
