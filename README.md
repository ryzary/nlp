# NLP Learning Notes

### Running The Notebooks using Docker

1. Build the Docker image
```
docker build -t nlp .
```
2. Run the Container
```
docker run -it -p 8888:8888 -v <host_path>:<container_path> <image_name>

ex:
docker run -it -p 8888:8888 -v /home/user/my_notebooks:/app/notebooks nlp
```
-   `-i` (interactive): Keeps the standard input open, allowing you to type commands.
-   `-t`: provides a terminal-like interface.
-   `-p 8888:8888`: Maps port 8888 for Jupyter Lab.
-   `-v /home/user/my_notebooks:/app/notebooks`: Mounts the `/home/user/my_notebooks` directory on your host to the `/app/notebooks` directory inside the container.


    You'll now be inside the container's Bash shell. You can run any Bash commands and use the Python environment you set up in the Dockerfile.

3. Running Jupyter Lab from inside the docker container

    If you want to run jupyter lab from inside the docker container after you have entered bash, you can run 
`jupyter lab --ip 0.0.0.0 --port 8888 --allow-root --no-browser`
. Then you can access the jupyter lab instance from your local browser by going to localhost:8888.

