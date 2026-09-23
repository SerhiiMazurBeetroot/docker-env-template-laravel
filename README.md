# docker-env Template for Laravel

This repository is the docker-env template for a Laravel site. It includes the Compose file, PHP Apache Dockerfile, and PHP config. `src/` is empty on purpose: docker-env runs `composer create-project` into it after the containers start.

The stack is PHP, MariaDB, phpMyAdmin, and Mailhog, on the shared `dockerwp` network. `{DOMAIN_NAME}` and `{DOMAIN_FULL}` in the Compose file and `.env.example` are replaced when a site is created.

## Usage

These files are used by docker-env. Clone that repository first:

```bash
git clone https://github.com/SerhiiMazurBeetroot/docker-env.git
```

The GitHub name docker-env uses for this template is `docker-env-template-laravel`.

## License

This project is licensed under the [MIT License](LICENSE).
