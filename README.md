# Jukebox Card for Home-Assistant

This is a media player UI for Home-Assistant leveraging the potential of the excellent new
[Lovelace UI.](https://www.home-assistant.io/lovelace/)

It allows you to configure a set of web radio stations (or possibly other radio media IDs such as spotify), and
play them to media player entities of your choice, like chromecast or spotify connect listeners.

This version supports multiple device types.

The device type [chromecast, sonos, yamaha] must be specified for each player (entity).

You can also specify a name to give the speaker if you do not want to use the friendly name.

## Acknowledgement
It's an improved version of the Jukebox https://github.com/lukx/home-assistant-jukebox

*Excerpt of ui-lovelace.yaml*
```
type: 'custom:jukebox-card'
links:
  - url: >-
      https://ruv-ras1-live-hls.secure.footprint.net/hls-live/ruv-ras1/_definst_/live.m3u8
    name: Rás 2
  - url: 'http://stream3.radio.is:443/tbylgjan'
    name: Bylgjan
  - url: 'http://stream3.radio.is:443/kissfm'
    name: Kiss FM
entities:
  - media_player: media_player.sonos_one
    type: sonos
  - media_player: media_player.google_mini_tv_room
    type: chromecast
    name: TV Room
  - media_player: media_player.yamaha_receiver_living_room
    type: yamaha
    name: Yamaha

```
