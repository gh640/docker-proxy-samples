# `docker-proxy-samples`

Samples to try Docker proxy feature.

## Prerequiresites

- Docker
- Docker Compose

## Usage

### 1. Build Docker images

```bash
docker compose build
```

### 2. Start `proxy` container

```bash
docker compose up proxy
```

### 3. Start `client` container and make requests

Open a new terminal and run the following command:

```bash
docker compose run --rm -it client python
```

```python
>>> import requests as r
>>> r.get('https://example.com')
<Response [200]>
```

You can see the proxy is used.
