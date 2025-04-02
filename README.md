# NLP Learning Notes

### Quick Start

1. Build the Docker image
```
docker build -t nlp .
```
2. Run the Container
```
docker run -it nlp
```
    The `-it` flags are essential:
-   i (interactive): Keeps the standard input open, allowing you to type commands.
-   t: provides a terminal-like interface.


    You'll now be inside the container's Bash shell. You can run any Bash commands and use the Python environment you set up in the Dockerfile.

3. Running Jupyter Lab from inside the docker container

    If you want to run jupyter lab from inside the docker container after you have entered bash, you can run 
`jupyter lab --ip 0.0.0.0 --port 8888 --allow-root --no-browser`
. Then you can access the jupyter lab instance from your local browser by going to localhost:8888.

