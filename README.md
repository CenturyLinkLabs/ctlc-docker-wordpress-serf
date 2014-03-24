ctlc-docker-wordpress-serf
==================

Base docker image to run a WordPress with Serf built-in


Usage
-----

To create the image `ctlc/wordpress-serf`, execute the following command on the ctlc-docker-wordpress-serf folder:

	sudo docker build -t ctlc/wordpress-serf .

Running the WordPress Container
------------------------

Run the `/run.sh` script to start WordPress (via Docker supervisor):

	ID=$(sudo docker run -d -p 80 ctlc/wordpress /run.sh)

It will store the new container ID (like `d35bf1374e88`) in $ID. Get the allocated external port:

	sudo docker port $ID 80

It will print the allocated port (like 4751). Test your deployment:

	curl http://0.0.0.0:4751/readme.html

Done!
