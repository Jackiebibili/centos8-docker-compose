## CentOS 8 Docker Remote Container
* This is a docker-compose file for running a virtual container of CentOS 8 _(ARM)_ on Docker.
* Initially, to pull and run the CentOS 8 image run `docker-compose up -d`. Then, the container will start running, and you can get into the CentOS by running `docker exec -it centos-container bash`, which will open an interactive STDIN on the bash shell.
* The container created is named `centos-container`.
* You are free to change the mount volumes to other directories on your host machine. Syntax for mount volumes is `[my-local-dir]:[virtual-dir]`.
* You can also commit the container changes to be stored in a new image by running `docker commit centos-container [new-image-name:version] [-m "message about this commit"]`. This will save the changes, so your modifications on the virtual system will not be lost when you remove the current container.
* For subsequent container startups, change the docker-compose image to the local image you committed.
* To use VS Code remote container, select `Open Folder in Container` in the commit palette. Then, choose the current folder, and VS Code will set everything up for you. [Read](https://code.visualstudio.com/docs/remote/devcontainerjson-reference) how to use devcontainer.json file.