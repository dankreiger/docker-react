### React Docker Setup

### build dev image

```sh
docker build . -f Dockerfile.dev
```

### map ports and run

bookmark node_modules volume and map into app folder

colon maps from inside to outside container - without colon just uses container

```sh
docker run -p 3000:3000 -v /app/node_modules -v $(pwd):/app IMAGE_ID
```
