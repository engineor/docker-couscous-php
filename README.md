Couscous PHP - Docker container
-------------------------------

This container has been created for development purpose.

## Usage

```
docker run --rm --interactive --tty -p=8000:8000 --volume $PWD:/app couscous-php preview 0.0.0.0:8000
```

## Integration in docker-compose

```
services:
  documentation:
    image: engineor/couscous-php
    ports:
      - "${EXTERNAL_PORT:-8000}:8000"
    volumes:
      - .:/app
    command: couscous preview 0.0.0.0:8000
```

## Limitations

The image has only been tested with `preview`. Support for any other command is not provided, but can be on demand.
