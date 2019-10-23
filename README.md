# Helm BlackBox Exporter

Ref:  https://github.com/prometheus/blackbox_exporter


###### Development Usage

```
docker run --rm -d -p 9115:9115 \
  --name blackbox_exporter \
  -v `pwd`:/config prom/blackbox-exporter:master \
  --config.file=/config/blackbox.yml

curl "http://localhost:9115/probe?target=www.example.com&module=http_2xx"
```


