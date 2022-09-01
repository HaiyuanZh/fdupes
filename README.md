# fdupes


inspired by https://github.com/coolcow/docker_fdupes#farmcoolcowfdupes



# I need fdupes run on arm envirement, so rebuild this image

 git clone https://github.com/HaiyuanZh/fdupes.git

 cd fdupes 

 docker build -f ./Dockerfile.entrypoints -t haiyuanzhang/entrypoints .

 docker build -f ./Dockerfile.fdupes -t haiyuanzhang/fdupes .

- again : if run on arm arch system , you have to re-run these for rebuild docker image

# usage not changed

```sh
docker run -it --rm \
  -e PUID=$(id -u $(whoami)) \
  -e PGID=$(id -g $(whoami)) \
  -v <PATH_TO_YOUR_DATA>:/data \
  haiyuanzhang/fdupes -r /data


Replace <PATH_TO_YOUR_DATA> with the directory-path of your data.

```
