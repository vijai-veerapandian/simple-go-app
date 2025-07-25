
##Run the simple Go Container application

### Build and Run locally
```
docker build -t simple-go-app .
```
```
docker run -d -p 8080:8080 simple-go-app:1.0.0
```

### Test the Local application

```
curl http://localhost:8080
```

## Push to GitHub Packages

```
docker tag simple-go-app ghcr.io/<vijai-veerapandian>/simple-go-app:1.0.0

```

### Push the docker image into the github package image repository

Log in to the GitHub Container Registry using your Personal Access Token (PAT).

```
export CR_PAT=COPIED_PAT
echo $CR_PAT | docker login ghcr.io -u <github-username> --password-stdin

docker push ghcr.io/<github-username>/simple-go-app:1.0.0
```

###