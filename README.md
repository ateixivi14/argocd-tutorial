# argocd-tutorial

1. Having an application image in docker hub
We need a repository in github which have a DockerFile. In this case, we will use this repository: https://github.com/ateixivi14/rover-api
We need to upload this image to docker hub, for that, after registiring we create a new repository:

<img width="1334" alt="Captura de pantalla 2023-03-17 a las 12 14 25" src="https://user-images.githubusercontent.com/77200940/225889582-99a628a5-dde7-44aa-a168-e01eb7ee5309.png">

We make sure that we have the image in local with the command:
docker images

Then we tag it 

`docker tag rover-api:latest ateixivi14/rover-api` 

And finally we push it:

`docker push ateixivi14/rover-api:latest`

<img width="736" alt="Captura de pantalla 2023-03-17 a las 12 18 38" src="https://user-images.githubusercontent.com/77200940/225890376-0a6a016f-4055-4b73-9dbe-586a32c2e102.png">

2. Install Minikube and set up

We will need to run these commands if we don't have Minikube installed:
```bash
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-darwin-amd64
sudo install minikube-darwin-amd64 /usr/local/bin/minikube
```
