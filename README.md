<h1 id="top" align="center">Monitor cAdvisor <br/> 🚢 v1.1.0 🚢</h1>

<br>

<div align="center">
    <img width=auto src="assets/banner/banner.png">
</div>

<br>

## 🔍 Table of Contents

- [Features](#features)
- [System Startup](#system-startup)

&nbsp; [![.Env](https://img.shields.io/badge/.ENV-ECD53F.svg?style=for-the-badge&logo=dotenv&logoColor=black)](https://www.ibm.com/docs/bg/aix/7.2?topic=files-env-file)

<br/>

<h2 id="features">🔥 Features</h2>

- **Docker Compose Deployment:** Simplifies deployment with Docker Compose configuration, enabling easy setup and service orchestration without complex commands.
- **.env Configuration:** All environment variables are easily configurable using the `.env` file, simplifying configuration management.
- **Network Setup:** Integrates cAdvisor with other metric tool networks.

<br/>

<h2 id="releases">🚢 Releases</h2>

&nbsp; [![.](https://img.shields.io/badge/1.2.0-233838?style=flat&label=version&labelColor=111727&color=1181A1)](https://github.com/ahmettoguz/monitor-cadvisor/tree/v1.2.0)

&nbsp; [![.](https://img.shields.io/badge/1.1.0-233838?style=flat&label=version&labelColor=111727&color=1181A1)](https://github.com/ahmettoguz/monitor-cadvisor/tree/v1.1.0)

&nbsp; [![.](https://img.shields.io/badge/1.0.0-233838?style=flat&label=version&labelColor=111727&color=1181A1)](https://github.com/ahmettoguz/monitor-cadvisor/tree/v1.0.0)

<br/>

<h2 id="system-startup">🚀 System Startup</h2>

- Create a new directory named `monitor`.

```
mkdir monitor
cd monitor
```

- Clone project.

```
git clone https://github.com/ahmettoguz/monitor-cadvisor
```

- Create `.env` file based on the `.env.example` file with credentails and configurations.

```
cp .env.example .env
```

- Create `network-monitor` network if not exists.

```
docker network create network-monitor
```

- Manage container.

```
docker stop                     container-cadvisor
docker rm                       container-cadvisor
docker compose -p monitor up -d service-cadvisor
docker logs -f                  container-cadvisor
```

- Refer to [`Node-Exporter`](https://github.com/ahmettoguz/monitor-node-exporter) repository to expose node metrics.

- Refer to [`Prometheus`](https://github.com/ahmettoguz/monitor-prometheus) repository to integrate prometheus to scrap metrics.

- Refer to [`Promtail`](https://github.com/ahmettoguz/monitor-promtail) repository to push traefik access logs to Loki.

- Refer to [`Loki`](https://github.com/ahmettoguz/monitor-loki) repository to scrap traefik access logs from promtail.

- Refer to [`Traefik`](https://github.com/ahmettoguz/proxy-traefik) repository to expose traefik access logs, metrics and also launch reverse proxy.

- Refer to [`Grafana`](https://github.com/ahmettoguz/monitor-grafana) repository to integrate grafana to visualize logs and metrics.

<br/>

### [🔝](#top)
