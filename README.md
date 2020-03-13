# json-serve
# Build previous image
$ docker build -t jsonserver .

# Run container
$ docker run --rm -it --name jsonserver-container -p 8080:8080 jsonserver


#Remote file:

$ docker run --rm --name jsonserver-container -p 8080:8080 -e "file=https://REMOTE_FILE.json" -it jsonserver

#Local file:

$ docker cp MY_LOCAL_FILE.json jsonserver-container:/tmp/test.json
