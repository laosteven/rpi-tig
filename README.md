# rpi-tig

Dockerized Telegraf/InfluxDB/Grafana for Rpi forked from [elafargue/rpi-tig](https://github.com/elafargue/rpi-tig).

> I just wanted a fire-and-forget way to quickly monitor a new Pi, this is it.

## Getting started

### Primary server

* Clone this repository;
* Run `./start.sh`.

### Secondary server

* Navigate to `/worker`;
* Copy the contents to your RPi;
* In `telegraf.conf`, make sure to update the `urls` of `[[outputs.influxdb]]` to the main server URL.

## Differences

* InfluxDB ports are exposed since different RPis will be reporting to the primary server.
* Telegraf monitors docker containers.
* Grafana port is set to `3010` instead of `3000`.

## Notes

Huge props to [elafargue](https://github.com/elafargue/rpi-tig) for cooking this up and to allow us to customize our dashboard monitoring instance to our heart content 🙇‍♂️.
