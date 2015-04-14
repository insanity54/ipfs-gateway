# ipfs-gateway
gateway for ipfs so you can run your site on the interplanetary file system


## what it do

* pull nginx docker image
* pull ipfs docker image
* barf a config file in /etc/nginx/sites-available


then what you do is something like

    docker run --name=ipfs-mydomain -p 8080:80 -e MYDOMAIN=example.com insanity54/ipfs-gateway

## github

for the Dockerfile and entrypoint junk go here:

https://github.com/insanity54/ipfs-gateway