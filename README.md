# WebRTC-DASH Ingestion

### Pull the ULL Server and Whip modules:

```
git submodule init
git submodule update
```

### Run:

```
docker-compose up --build
```

Wait until everthing initialized. It takes a couple of seconds until the
eyevinn WHIP endpoint is initialized.

### GoTo:

```
http://localhost:1234
```

Click the Camera or Screen button to start the WebRTC stream.

I takes a couple of seconds until the necessary manifest file is created.

### CAVEAT

If you want to restart the media ingestion process, please refresh 
`http://localhost:1234` to destroy the existing socket to the ULL server.
A new FFMPEG instance will be created automatically, and it will wait for
input. Old chunks will be deleted.

### Output:

By navigating to `http://127.0.0.1:8080/`, you can find the manifest files (with
and without the WebRTC link) and the created chunks.

The dash.js client plays the the `manifestWebrtc.mpd` file. 

### How to play this content?

Clone our fork of the dash.js player.

Start the dash.js player and follow the insructions in the repository.
