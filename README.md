# docker-cypress-japanese

Cypress docker image with browsers and japanese locale.

You can use these tags as base cypress image version.

- `browsers-node11.13.0-chrome73`

## Example Usage

`docker-compose.yml`

```yaml
version: 3.6
services:
  app:
    image: shufo/cypress-japanese:browsers-node11.13.0-chrome73
    volumes:
      - "./:/app"
      - ".cache:/root/.cache"
    container_name: app
    working_dir: "/app"
    tty: true
```

Install cypress binary

```bash
$ docker exec -it app yarn run cypress install
```

Generate example cypress test

```bash
$ docker exec -it app yarn run cypress open
```

Run test

```bash
$ docker exec -it app yarn run cypress run
```
