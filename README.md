# How to create a container image and push to ECR

1. Create Dockerfile and application code
2. `docker build -t <registry url>/<repo>:<tag>`: build image
3. `aws ecr get-login-password --region "<region>" | docker login --username AWS --password-stdin <account id>.dkr.ecr.<region>.amazonaws.com/<repo>`: connect AWS CLI to ECR registry
4. `docker push <registry url>/<repo>:<tag>`: push the image to the registry
