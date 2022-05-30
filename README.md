# pihole-cloudflared-docker

> Pi-hole and cloudflared in Docker via `docker-compose`

## Getting Started

Assuming you have Docker installed...

1. Clone this repo:

```shell
git clone https://github.com/thegreatsunra/pihole-cloudflared-docker.git
cd pihole-cloudflared-docker
```

2: Set up internal network:

Change the `--subnet` and `--gateway` values to match the configuration of your own network.

```shell
sudo docker network create -d macvlan \
  --subnet=192.168.2.0/24 \
  --gateway=192.168.2.1 \
  -o parent=eth0 priv_lan
```

TODO: Configure this internal network via `docker-compose.yml`

## Usage

1. Copy `./example.env` to `./.env` and update the variable values it contains as suits your purposes.

2. From the project root, run the whole thing:

```shell
docker-compose -p pihole up -d
```

## License

MIT
