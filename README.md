# prometheus-dash-exporter 

Prometheus exporter for the DASH cryptocurrency using the [Cryptonator](https://www.cryptonator.com/) API.

This is a simple server that scrapes DASH value in EUR from the cryptonator.com API.
POC project to get me started with python3.

## Requirements
prometheus_client (pip3 install prometheus_client)

## Config values
- http_port = tcp/listener, default: 9091
- interval = refresh values every x seconds, default 60

## Exported metrics
- dash_value_in_EUR
- dash_value_change
- dash_value_timestamp

## prometheus example config
```yaml
  - job_name: 'dash'
    scrape_interval: 60s
    static_configs:
            - targets: ['localhost:9091']
```

## License

MIT License, Copyright (c) 2020
[Stefan Funke](https://itgaertner.net)
