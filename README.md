# pihole-cloudflared-docker

> Pi-hole and cloudflared in Docker via `docker-compose`

## Usage

### TODO: Configure internal network via `docker-compose.yml`

```shell
sudo docker network create -d macvlan \
  --subnet=192.168.2.0/24 \
  --gateway=192.168.2.1 \
  -o parent=eth0 priv_lan
```

## License

MIT
