# Cron Image With Python

## Overview

This Docker image provides cron job. It is built on Alpine and includes Python.

## Quick Start

To build the image:

```bash
docker build -t cron-python src
```

To run the image:

```bash
docker run -d \
    --restart unless-stopped \
    -v "$(pwd)/src/data/script.py:/scripts/script.py" \
    -v "$(pwd)/src/data/cron.crontab:/etc/crontabs/root" \
    -e TZ=Europe/Paris \
    --name <your-container-name> \
    cron-python
```

To get logs:

```bash
docker logs <your-container-name>
```

## Contributing

Contributions to this Docker image are welcome. Please submit a pull request or issue on the repository.

## License

MIT License
