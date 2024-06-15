# How To Execute Applications using the Orchestrators
> This assumes that the images have already been created and stored in a container registry (in my case DOCKERHUB)

## Orchestrator 1: Using Docker Compose
### Prerequisites
- Ensure Podman and Podman compose have already been installed to the machine where you want to run it
- Choose (create a new folder) of choice and store the [docker compose YAML file](docker-compose.yml) there
- Next to this file, create a folder `/config` with a file named `.env` in it
  - Within the created file, set the properties for:|
    - MYSQL_ROOT_PASSWORD
    - MYSQL_DATABASE
    - MYSQL_USER
    - MYSQL_PASSWORD
- Then execute the following command:
  `podman-compose --env-file ./config/.env up -d`