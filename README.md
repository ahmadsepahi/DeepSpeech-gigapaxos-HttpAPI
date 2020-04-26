# DeepSpeech-gigapaxos-HttpAPI

Pull the docker: docker pull ahmadsepahi/deepspeech_orig:latest

git clone https://github.com/MobilityFirst/gigapaxos

cd gigapaxos

ant jar

```
bin/gpServer.sh -DgigapaxosConfig=conf/examples/http.properties start all
```
```
docker run -p 8000:8000 --network="host" --name deepspeech ahmadsepahi/deepspeech:latest
```

upload an audio file with 16Khz frequency via browser or terminal

- Browser: http://localhost:8000/ -> upload file -> the result will be presented

- Terminal: curl -F file=@your_audio_file.wav http://localhost:8000
