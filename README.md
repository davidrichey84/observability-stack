# observability-stack
Prometheus / Grafana / Thanos / Telegraf observability stack

This is a WIP! Its in a very raw form right now so you will need to guide yourself a bit. 

If you want the python prom injector running for instance, build the container and add it to the docker-compose. 

## Up and Running

`docker-compose up`

### Start Select Components
Example:
`docker-compose up grafana minio loki`

## Services and Their Ports
| Service | Port  | Link   |
| ------- | ----- | ------ |
| Grafana | 3000 | [Grafana](http://localhost:3000)|
| Minio   | 9000 | [Minio](http://localhost:9000) |
| Prometheus | 9090 | [Prometheus](http://localhost:9090) |
| Thanos Query | 10904, 10903 (gRPC) | [Thanos Query](http://localhost:10904) |
| Thanos Query-FE | 10999 | [Thanos Query-FE](http://localhost:10999) |
| Thanos Store | 10905 (gRPC) | None |
| Thanos Receive 1 | 10907 (gRPC), 10908 (Remote Write) | None |
| Alertmanager | 9093 | [Alertmanager](http://localhost:9093) |
| Loki | 3101 | None |
| Telegraf | 9273 (prom metrics) | None |

## Grafana Datasources
Screenshot will have to do for now
![alt text](https://raw.githubusercontent.com/davidrichey84/observability-stack/main/images/grafana_config.png)