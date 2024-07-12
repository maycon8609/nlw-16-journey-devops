## Kubernetes

### create k3d cluster
```sh
  k3d cluster create nlw-journey --servers 2
```

### create namespace
```sh
  kubectl create namespace journey
  kubectl create ns journey-helm
```

### apply config on namespace
#### `-f : file to manifest, -n : namespace`
```sh
  kubectl apply -f k8s/deployment.yaml -n journey
  kubectl apply -f k8s/secret.yaml -n journey
```

## Terraform

### init and plan
```sh
  terraform init
  terraform plan
```

### apply
```sh
  terraform apply -auto-approve
```

### destroy cluster
```sh
  terraform destroy -auto-approve
```

## Helm

### start
#### `helm create DIRECTORY-NAME`
```sh
  helm create deploy
```

### apply manifest to helm
```sh
  helm upgrade --install journey ./deploy -n journey-helm
```