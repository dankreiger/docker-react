# docker-react

[![Build Status](https://travis-ci.org/dankreiger/docker-react.svg?branch=master)](https://travis-ci.org/dankreiger/docker-react)

## Development

### build dev image

```sh
docker-compose up --build
```

### run docker compose

```sh
docker-compose up
```

### Manual without docker compose

### build dev image

```sh
docker build . -f Dockerfile.dev
```

##### map ports and run

bookmark node_modules volume and map into app folder

colon maps from inside to outside container - without colon just uses container

```sh
docker run -p 3000:3000 -v /app/node_modules -v $(pwd):/app IMAGE_ID
```

### run tests

```sh
docker run -it IMAGE_ID npm run test
```

## Prod

```sh
docker build . # get image id at end
docker run -p 8080:80 IMAGE_ID # visit localhost:8080
```
