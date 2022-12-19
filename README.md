# airtouch2p-nodered-mqtt

Beginnings of Node RED flow to sit between an Polyaire AirTouch 2+ controller and Home Assistant via MQTT

## Development

- [x] Status
  - [x] AC
  - [ ] Groups
  - [ ] Extended Messages
- [ ] Control
  - [ ] AC
  - [ ] Groups

## Instructions

1. Import the flow.json
1. Set your AirTouch 2+ controller IP on the two TCP nodes
1. Set your MQTT broker configuration
1. Check MQTT and wait for status message, or hit 'Status Message' inject on flow

## MQTT Topic

States will be published to:

```home/airtouch2p/<AC Number>/#```

If you only have one AC, this should be:

```home/airtouch2p/0/#```

To see any messages, subscribe to:

```home/airtouch2p/#```

# Home Assistant

## Configuration

To use the built-in climate card, add the `mqtt` configuration to your favourite location, best to try `configuration.yaml` first and move it later.

https://github.com/thesheehans/airtouch2p-nodered-mqtt/blob/main/mqtt_configuration.yaml

![Screenshot of Home Assistant Climate Card](https://github.com/thesheehans/airtouch2p-nodered-mqtt/blob/1c24ee8470e3843778ca4f312a456b5ba343498b/climate.png)
