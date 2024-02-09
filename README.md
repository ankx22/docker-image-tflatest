# Docker Image for Tensorflow latest with latest CUDA 
Has most basic dependencies and more can be added by modifying the [Dockerfile](Dockerfile)

- To run the docker container:
	- Clone the repo
  - In the repo folder open a bash terminal and run
    ```bash
    docker build -t tflatest .
    ```
  - Once the download and setup of the image is complete just run the docker image by
    ```bash
    docker run -it --rm -p 8888:8888 -v /actual/path/to/data:/data --name name_of_the_container -e DISPLAY=$DISPLAY -v /tmp/.X11-unix:/tmp/.X11-unix tflatest
    ```
  - To access the bash on a different terminal window run
    ```bash
    docker exec -it <container_id_or_name> /bin/bash
    ```
  - To access the jupyter notebook on any browser just navigate to
    [https://localhost:8888](https://localhost:8888)
    

## Maintained by
Ankit Talele - amtalele@wpi.edu
