# flamescope-build

This is a containerized version of flamescope.

## Build
```
docker build --rm -t taion809/flamescope-build
```

## Usage

You can pull down your perfomance samples locally and mount a volume to the container to visualize.

```bash
docker run \
  --rm \
  -e "FLAMESCOPE_STACK_DIR=samples" \
  -p 5000:5000 \
  -v `pwd`/samples/:/usr/src/app/samples \
  taion809/flamescope-build
```
