# Dockerfile Bug: Missing requirements.txt
This repository demonstrates a common error in Dockerfiles: attempting to use a file that's not included in the build context.

## The Bug
The provided Dockerfile attempts to install dependencies using `pip3 install -r requirements.txt`. However, the `requirements.txt` file is missing from the build context. This results in a build failure.

## The Solution
The solution involves adding the `requirements.txt` file to the build context and ensuring it's correctly copied into the image before running the installation command.

## How to Reproduce
1. Clone this repository.
2. Try to build the image using `docker build -t my-app .`
3. Observe the build failure.
4. Refer to the `DockerfileSolution.txt` for the corrected Dockerfile.