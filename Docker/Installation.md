# Install from a package

Go to [Docker Distributions](https://download.docker.com/linux/ubuntu/dists/), choose your Ubuntu version, browse to pool/stable/ and choose amd64, armhf, ppc64el, or s390x. Download the .deb file for the Docker version you want to install.

Install Docker CE, changing the path below to the path where you downloaded the Docker package.

> sudo dpkg -i /path/to/package.deb

The Docker daemon starts automatically.

Verify that Docker CE is installed correctly by running the hello-world image.

> sudo docker run hello-world

This command downloads a test image and runs it in a container. 
When the container runs, it prints an informational message and exits.

Docker CE is installed and running. 
The docker group is created but no users are added to it. You need to use sudo to run Docker commands.

## Post-installation steps for Linux

Create the docker group.

> sudo groupadd docker

Add your user to the docker group.

> sudo usermod -aG docker $USER

Log out and log back in so that your group membership is re-evaluated.

Verify that you can run docker commands without sudo.

> docker run hello-world

This command downloads a test image and runs it in a container. 
When the container runs, it prints an informational message and exits.
