## Build docker image (Compiles everything, will take a while)
`docker build -t locality-img .`

## Add ollama in the container

`docker compose up -d`

## Access ollama commands from the container

`docker compose exec ollama bash`

## Install LLM using ollama

`ollama run llama3.2:latest`

## To exit from the CLI LLM

`/bye`

## Visit this to access Librechat with ollama running

`http://localhost:3080/`

## Visit this to access mongo-express (not supported yet, maybe will add later)

`http://localhost:8081/`

username: admin

password: password

## To stop librechat, in the docker bash:

`exit`

`docker compose down`

---

# DEVELOPMENT

After modifying a react component, will need to rebuild the image. 
`docker build -t locality-img .`

If modification was only made to .yaml .yml files, then `docker compose up` is suffice