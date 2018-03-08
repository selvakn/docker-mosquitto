docker-mosquitto
================

Mosquitto MQTT Broker on Docker Image with auth plugin

## Build

$ ```docker build --no-cache -t selvakn/mosquitto:v1.4.15 .```

## Mapping host directories

    $ sudo docker run --rm -ti \
      -v `pwd`/etc/mosquitto.d/auth-plugin.conf:/etc/mosquitto.d/auth-plugin.conf \
      --name mqtt \
      -p 1883:1883 \
      -p 9883:9883 \
      selvakn/mosquitto:v1.4.15
