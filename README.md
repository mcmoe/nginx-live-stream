# nginx-live-stream

The docker image for nginx rtmp hls server and a html5 player to monitor the live brocasting.
Build on Alpine with [nginx rtmp module](https://github.com/arut/nginx-rtmp-module) and [video.js](https://github.com/videojs).

# How to use
```
docker-compose up -d
```
or
```
docker run -p 80:80 -p 1935:1935 -d mcmoe/nginx-live-stream
```


The `80` port is for video player, it will autoplay when stream source is ready.
The `1935` port is for encoder clients like 
* [OBS](https://obsproject.com/)
* [VLC media player](https://www.videolan.org/)
* or a webcam device

Use the following URL to publish your streams: rtmp://{{host}}/live/{{stream name}}

The __Stream key__ input whatever you like. And don't use __Authentication__ option.
