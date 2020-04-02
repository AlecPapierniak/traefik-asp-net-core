# example of using traefik in front of an aspnetapp

## run 
`docker-compose up -d`

## add the necessary hostfile entries
add these two lines to your hostfile:

`127.0.0.1		whoami.localhost`

`127.0.0.1		aspnetapp.localhost`

## test the apps
open up your browser and visit:

* `http://localhost:5000` <-- this is the aspnetapp, being access directly (not going through traefik)
* `http://whoami.localhost` <-- this is the whomai container, going through treafik
* `http://aspnetapp.localhost` <-- this is the aspnetapp container, going through treafik