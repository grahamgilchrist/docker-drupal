# docker-drupal

Dockerfile repo for a php and apache container for running Drupal 6-7 sites

Available from the the docker hub regsitry as `grahamgilchrist\drupal`

## Background
Repo structure is based on the same version folder convention as official docker hub repos (e.g. python: https://github.com/docker-library/python)

# Use with docker compose:
`docker-compose.yaml`:
```
drupal:
  image: grahamgilchrist/drupal
  volumes:
    - ./project:/var/www/html
  links:
    - db
  ports:
    - "8000:80"  
```
* `docker-compose up drupal`
