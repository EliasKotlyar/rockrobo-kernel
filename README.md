# Trying to compile modules for rockrobo

```
# Build kernel within docker image
docker build -t rockrobo-kernel .

# Get wifi kernel module out
docker rm -f rockrobo-kernel || true
docker create --name rockrobo-kernel rockrobo-kernel:latest
docker cp rockrobo-kernel:/usr/src/rtl8812au/8812au.ko .
```