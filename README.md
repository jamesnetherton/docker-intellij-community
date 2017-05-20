# docker-intellij-community

[IntelliJ](https://www.jetbrains.com/idea/) community edition running on Docker.

## Building the image

Clone this repository, change into the source directory and run:

```
docker build -t yournamespace/yourimagename:yourtag
```

## Running IntelliJ

To run do the following to share your X11 socket with the IntelliJ container:
```
docker run -it \
  -v /tmp/.X11-unix:/tmp/.X11-unix \
  -e DISPLAY=unix$DISPLAY \
  jamesnetherton/intellij-community
```
