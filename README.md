# docker-conquest
Docker container implementing version 1.4.17d of the [ConQuest DICOM server]. 

[ConQuest DICOM server]: <https://ingenium.home.xs4all.nl/dicom.html>

### About
This is a Docker-ised version of the fabulous ConQuest DICOM Server, built on top of a base Ubuntu 14.04 LTS (Trusty Tahr) image.  Another version based on Ubuntu 16.04 (Xenial Xerus) will also be implemented after its release.

### Installation
If you want to build from the Dockerfile, simply copy this to a folder on your local machine, open a terminal in that folder and type:
```sh
$ sudo docker build -t docker-conquest .
```
Then, to run the Docker image, simply run:
```sh
$ sudo docker run -p 5678:5678 -p 80:80 docker-conquest
```
Note that this will bind ports 5678 and 80 in the Docker container to the same ports on the host.  Change these if you want them bound elsewhere.

### Ports
The following ports are exposed: 
  - Port 5678 - used for DICOM send/query/receive.
  - Port 80 - used for http.

### Licence
MIT Licence for Dockerfile.
ConQuest DICOM server is licensed separately (see [LICENSE] file).

[LICENSE]: <LICENSE>

### Issues
Please report any issues and I'll get to them ASAP.



