# How to Run the Docker Container

Follow the steps below to run the Docker container for the "Tween Agency" website:

1. **Build the Docker Image:** 
    If you haven't already built the Docker image, follow these steps:

    ```bash
    docker build -t tween-agency-web-server .
    ```

    The above command will create a Docker image named `tween-agency-web-server`.

2. **Run the Docker Container:**
    Now, run the Docker container using the following command:

    ```bash
    docker run -d -p 80:80 --name tween-agency-container tween-agency-web-server
    ```

    This command will start a Docker container named `tween-agency-container` based on the previously built image.

3. **Access the Website:**
    Open your web browser and visit `http://localhost`. You should see the "Tween Agency" website template.

4. **Stop the Docker Container:**
    If you want to stop the Docker container, execute the following command:

    ```bash
    docker stop tween-agency-container
    ```

    This command will stop the running container.

