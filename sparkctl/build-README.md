# Tdac Build
To build this go application you need to run this command from the main folder of the project

```bash
docker buildx build --platform linux/amd64 -t 110217436165.dkr.ecr.eu-west-1.amazonaws.com/sparkctl:<tag> -f Dockerfile.sparkctl .
```

after that you need to login on docker to push the image on ecr

```bash
aws ecr get-login-password | docker login --username AWS --password-stdin 110217436165.dkr.ecr.eu-west-1.amazonaws.com
docker push 110217436165.dkr.ecr.eu-west-1.amazonaws.com/sparkctl:<tag> 
```
