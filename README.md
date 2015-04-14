# ipfs-gateway
gateway for ipfs so you can run your site on the interplanetary file system

## NOTE

This is totally broken right now. Don't use it. It's half repo, half automated build, half I don't know what I'm doing. I'm just messing around, figuring stuff out. Don't use this version.


## what it do

It builds a docker image of an nginx instance that's ready to proxy your ipfs

What you do is something like

    docker run -d --name=ipfs -p 4441:4001 jbenet/go-ipfs
    docker run -d --name=nginx-ipfs -v /media/srv/nginx:/etc/nginx/conf.d:ro -p 80:80 --link=ipfs:ipfs nginx

## github

for the Dockerfile and junk go here:

https://github.com/insanity54/ipfs-gateway


## TODO

- [ ] make the damn thing build without err
- [ ] figure out better solution for hardcoded 'ipfs' hostname in nginx config (nginx container is meant to link to ipfs container)
- [ ] add mechanism to pin a hash sent as an env var. This would be used to mirror the site on this node
- [ ] add docker compose script for those who aren't using systemd
