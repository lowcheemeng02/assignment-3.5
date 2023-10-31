# How to create a container image and push to ECR

1. `docker build -t <registry url>/<repo>:<tag>`: build image
2. `aws ecr get-login-password --region "<region>" | docker login --username AWS --password-stdin <account id>.dkr.ecr.<region>.amazonaws.com/<repo>`: connect AWS CLI to ECR registry
3. `docker push <registry url>/<repo>:<tag>`: push the image to the registry
