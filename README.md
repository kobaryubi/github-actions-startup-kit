# github-actions-startup-kit
### Create a Docker repository
```bash
gcloud artifacts repositories create quickstart-docker-repo --repository-format=docker --description="Docker repository" --location=us-west2
gcloud artifacts repositories list
```

### Build an image using Dockerfile
```bash
gcloud builds submit --region=us-west2 --tag=us-west2-docker.pkg.dev/my-own-pace/quickstart-docker-repo/quickstart-image:tag1
```

### Build an image using a build config file
```bash
gcloud builds submit --region=us-west2 --config cloudbuild.yaml
```

### Delete a repo
```bash
gcloud artifacts repositories delete quickstart-docker-repo --location=us-west2
```
