# Notes

`git clone https://git.ittavern.com/CaffeineFueled/podman-compose-grafana-loki.git`

*Github users, feel free to change this URL!*

`cd podman-compose-grafana-loki`

`podman compose up -d`

Taking it down:

`podman compose down`

Check status:

`podman container ps -a`

> Note: not ready for production!

## Endpoint

**Grafana** `http://localhost:3000`

Check:

```bash
curl -Ls 127.1:3000 | grep '<title>'

# <title>Grafana</title> ✅
```

**Loki** `http://localhost:3100`

Check:

```bash
curl -Ls 127.1:3100/ready

# ready ✅
```

*from the perspective of the host!*

## Auth

Open Grafana in your browser, default creds are `admin`/`admin`.

## Data Source

Loki should be already available as datasource. Edit `./grafana/datasources/ds.yml` to make changes!

# TODO

- [ ] Authentication for Loki
- [ ] Add names to the containers (maybe)
