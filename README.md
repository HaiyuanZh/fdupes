# fdupes


inspired by https://github.com/coolcow/docker_fdupes#farmcoolcowfdupes



# I need fdupes run on arm envirement, so rebuild this image

 docker build -f ./Dockerfile.entrypoints -t haiyuanzhang/entrypoints .

 docker build -f ./Dockerfile.fdupes -t haiyuanzhang/fdupes .


# usage not changed

```sh
docker run -it --rm \
  -e PUID=$(id -u $(whoami)) \
  -e PGID=$(id -g $(whoami)) \
  -v <PATH_TO_YOUR_DATA>:/data \
  haiyuanzhang/fdupes -r /data


Replace <PATH_TO_YOUR_DATA> with the directory-path of your data.
```