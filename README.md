# Nginx-rtmp-hls
Docker image to run an Nginx RTMP/HLS server.

NGINX Version 1.10.3
nginx-rtmp-module Version 1.1.10

### Running

Use the following command to run the container and bind the port 1935 and 80 to the host machine:
```
docker run -p 1935:1935 -p 80:80 shaneen31/nginx-rtmp-hls
```

### OBS Studio Configuration
Under Settings > Stream, set the follwing parameters:
```
Streaming Service: Custom streaming server
Server: rtmp://<Server ip>/live
Stream Key: <Stream key>
```

### Streaming URLs
rtmp://&lt;Server ip&gt;/live/&lt;Stream key&gt;
http://&lt;Server ip&gt;/hls/&lt;Stream key&gt;.m3u8
