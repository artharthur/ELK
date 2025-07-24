# Домашнее задание: ELK (Elasticsearch, Logstash, Kibana)

## Задание 1: Elasticsearch

- Поднят Elasticsearch в Docker через `docker-compose`
- Установлен уникальный `cluster_name`: `elk-homework-cluster-artnet`
- Elasticsearch успешно запущен и отвечает на запросы

### Проверка кластера:

bash
curl -X GET 'localhost:9200/_cluster/health?pretty'

### Скриншот результата

![Cluster Health](./screenshots/elasticsearch-cluster-health.png)

---

## Задание 2: Kibana

- Установлена Kibana через `docker-compose`
- Интерфейс Kibana доступен на http://localhost:5601
- В разделе **Dev Tools** выполнен запрос к кластеру:

http
GET /_cluster/health?pretty

### Скриншот результата

![Kibana Cluster Health](./screenshots/kibana-cluster-health.png)

---

## Задание 3: Logstash + Nginx

- Установлены и запущены Logstash и Nginx через `docker-compose`
- Logstash читает `access.log` и передаёт данные в Elasticsearch
- В Kibana создан индекс `nginx-logs`, данные визуализируются

### Скриншот интерфейса Discover

![Nginx Logs in Kibana](./screenshots/kibana-nginx-logs.png)
