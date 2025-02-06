# Development

## URLs for testing

http://icecast.omroep.nl/radio1-bb-mp3
spotify:album:3DrgM5X3yX1JP1liNLAOHI
spotify:track:2UWdUez9MB9yzL7Y81Mcip
spotify:track:47vmcuvMWFIsMaiHFIGSIu

## Getting Spotify to work and testing

DEB package: https://github.com/kingosticks/gst-plugins-rs-build/releases/tag/gst-plugin-spotify_0.14.0-alpha.1-1

See documentation how to obtain an access token: https://gitlab.freedesktop.org/kingosticks/gst-plugins-rs/-/blob/spotify-access-token-logging/audio/spotify/README.md

Test the GStreamer Spotify plugin:
```sh
SPOTIFY_TOKEN=BQAldsYgZRcBdWgMq3un09w3YrGOaPmLr_CNJvS540s73vGpu0dXYa4yQkdBodmw5ogncwhecJAZPC5Nss74O2iuKG_e59g7ccZJKS7EpKnbdVIO-1tAbJJ-v1i0d9su9vDGzy6RLQXEtB6OEX2CcD0N9qAcOvHYW5K6s8zTOn9124mGyHJPq_z7f0HUPfqDALBtre0NKrTtufF2JZY8Hj3QCoyGDtgPVfdPTmR9
GST_DEBUG=librespot:6 gst-launch-1.0 spotifyaudiosrc access-token=$SPOTIFY_TOKEN track=spotify:track:2UWdUez9MB9yzL7Y81Mcip ! oggdemux ! vorbisdec ! audioconvert ! autoaudiosink
```

## Old stuff

I had this in /etc/hosts on the Raspberry Pi for a while and removed it on 2025-02-06:
> # See https://github.com/librespot-org/librespot/issues/972
> # Can hopefully be removed once upgraded to librespot 0.4.2
> # IP of ap-guc3.spotify.com
> 104.154.127.126         ap-gew4.spotify.com
