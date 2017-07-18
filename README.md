# hospitaliplus-server

cd to hospitalrun-server folder

run `docker-compose up --build -d` (in some case add --force-recreate to generate new containers)

use the mapped folders to tweak the settings inside

run docker ps to list all running containers

drop to the shell of the couchdb container using it's id from previous step

get it's ip address by typing `ip addr` --ensure it running and listening on port 5984


change the ip address on the initcouch.sh script on the host machine, this changes the file too in the container as it's mounted, do the same for config.js 

drop to the hospitalrun shell and run the initcouch.sh script to bootstrap the whole application ....

finally replace the original config.js with the updated one ....


the last three steps can be eliminated by having nano as part of the image