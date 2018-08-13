# Docker Image for Vertica 9 Community Edition

The image is available on dockerhub at https://hub.docker.com/r/iamamr/vertica/

Base OS is Debian 9.2.

## Usage:
### Pull the image from Docker Registry:

```bash
docker pull iamamr/vertica
```

#### Build your own Image:

- Download the Vertica DEB package from https://my.vertica.com and put it in this folder as "vertica9.deb".

    Then run:

    ```bash
    docker build -t iamamr/vertica .
    ```

### To run without a persistent datastore
```bash
docker run -p 5433:5433 iamamr/vertica
```

### To run with a persistent datastore
```bash
docker run -p 5433:5433 -d -v /path/to/vertica_data:/home/dbadmin/docker iamamr/vertica
```
### Connection Parameters
 Default DB Name - docker
 
 Default User - dbadmin
 
 Default Password (NO PASSWORD) - 