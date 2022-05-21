# rpi-tig

## Secondary server setup

Creates a Telegraf container that reports to the main server.

## Getting started

The `telegraf.conf` file is the same as the main server one.

Make sure to edit the URL to the correct endpoint:

```conf
[[outputs.influxdb]]
  urls = ["http://influxdb:8086"]
```

Once edited, run `docker-compose up -d`.
