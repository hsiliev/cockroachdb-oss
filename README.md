# cockroachdb-oss
CockroachDB OSS Docker image

## Using CockroachDB

```sh
docker-compose up
```

Connect to the UI on http://localhost:8080

To stop the running container(s), either use Ctrl-C or:
```sh
docker-compose down
```

## Rebuild the image

```sh
./clean
./publish <your Docker Hub repo name>
```
