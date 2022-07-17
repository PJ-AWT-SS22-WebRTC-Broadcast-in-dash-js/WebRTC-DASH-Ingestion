# WebRTC-DASH Ingestion

### Pull ull and whip:

```
git submodule init
git submodule update
```

### Run:

(If you are restarting, please refresh `http://localhost:1234` to destroy
the existing socket to ull server.)

```
docker-compose up --build
```

### GoTo:

```
http://localhost:1234
```

Click the Camera or Screen button to start the WebRTC stream.
