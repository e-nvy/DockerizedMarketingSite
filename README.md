# Marketing Project - Docker Image

This Docker image sets up an Apache web server hosting a project named "Marketing" based on a template from www.tooplate.com.

## Dockerfile Explanation

The Dockerfile consists of two stages:

### 1. BUILD_IMAGE Stage
- Uses the `ubuntu:latest` base image to build the project.
- Installs `wget` and `unzip`.
- Downloads the template ZIP file from https://www.tooplate.com/zip-templates/2128_tween_agency.zip.
- Extracts the template contents, compresses them into a tar.gz file, and moves it to `/root/tween.tgz`.

### 2. Final Stage
- Uses the `ubuntu:latest` base image again for the final image.
- Installs Apache2, Git, and wget.
- Copies the `tween.tgz` file from the BUILD_IMAGE to `/var/www/html/`.
- Extracts the contents of `tween.tgz` in `/var/www/html/`.
- Starts the Apache2 web server, serving the Marketing project.

## How to Build the Docker Image

To build the Docker image, follow these steps:

1. Save the provided Dockerfile to a directory on your local machine.
2. Open a terminal or command prompt and navigate to the directory containing the Dockerfile.
3. Run the following command to build the image:

   ```bash
   docker build -t marketing_project .

