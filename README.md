# My own Django starter

- Docker & Docker Compose
- Nginx & SSL (Let's Encrypt)
- PostgreSQL
- Django
- Gunicorn

## Install (first usage)
1. Fork this project (or download the master.zip)
2. Delete the `.git` folder
3. Rename the folder to your project name
4. Execute `install.sh` and provide your project name

## Usage
Run `docker-compose up`

## Deploy
1. Edit `deploy.sh` and `docker-compose.prod.yml` with your project envvars (`USER`, `SERVER_URI`, `VIRTUAL_HOST`, `LETSENCRYPT_HOST` and `LETSENCRYPT_EMAIL`)
2. Run `./deploy.sh`

### Deploy to other environments
You can copy and rename `docker-compose.prod.yml` replacing `prod` to `dev`, for example, and do the same with `deploy.sh` (in this example will be something like `deploy.dev.sh`) and change the lines that make sense to you to deploy to any enviroment that you have.


## Roadmap
- [ ] Update `DATABASE` in `settings.py` on install to connect with the `database` service
