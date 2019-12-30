# Notes

```sh
docker run -d -p 9000:9000 --name portainer --restart always -v /var/run/docker.sock:/var/run/docker.sock portainer/portainer


sudo docker swarm init
docker stack deploy --prune -c $(pwd)/docker-compose.yml tick

docker stack services tick
docker stack rm tick

docker service ls
docker service ps --no-trunc
```

```sh
curl -i -XPOST http://localhost:8086/query --data-urlencode "q=CREATE DATABASE mydb"
while true
do
curl -i -XPOST 'http://localhost:8086/write?db=mydb' --data-binary 'alarm_test,host=server01 value=3.64'
sleep 1
done
```