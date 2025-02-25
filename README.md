# Element Web Docker Container

This repository provides a Docker image for running [Uni-Link](www.localhost) (Powered by [Element](https://element.io), a modern web client for the [Matrix](https://matrix.org/) protocol. The image is available on Docker Hub as [`rohitrajt1/element-web`](https://hub.docker.com/r/rohitrajt1/element-web).

## Prerequisites

- **Docker:** Make sure you have Docker installed and running. You can download it from [Docker's official website](https://www.docker.com/get-started).
- **Docker Hub Account (optional):** Required if you plan to pull or push customized images.

## Running the Container

To start the Element Web container, execute the following command:

```bash
docker run -d -p 80:80 rohitrajt1/element-web:latest
```
-d: Runs the container in detached mode.
-p 80:80: Maps port 80 on your host machine to port 80 in the container. Adjust these ports if necessary.
Once the container is running, open your browser and go to http://localhost (or your host's IP/domain) to access Element Web.

## Configuration and Environment Variables
- Element Web may require specific environment variables for proper configuration. You can pass these variables at runtime using the -e flag. For example, to set your homeserver and identity server URLs, run:

```bash
docker run -d -p 80:80 \
  -e REACT_APP_DEFAULT_HS_URL=https://your-homeserver.com \
  -e REACT_APP_DEFAULT_IS_URL=https://your-homeserver.com \
  rohitrajt1/element-web:latest
```

## Troubleshooting
- **Image Not Found**: Ensure that the image was tagged correctly. Verify your local images with:

- **Port Conflicts**: Check that the host port (e.g., port 80) is not already in use.

Logs:
If the container isn't running as expected, inspect the logs using:
```bash
docker logs <container_id>
```
- **Environment Variables**: Verify that all necessary environment variables are set correctly.

## What Next?
- Open www.localhost for running the element instance.
- Create a new account (Cant be done as of now as server is localhost).
- Navigate to college hub.
- Interact

  ## ScreenShots

  - General Chat
  ![image](https://github.com/user-attachments/assets/5a570711-21b2-410a-875c-2c5e74d0fbfa)
  - Matrix Server
  ![image](https://github.com/user-attachments/assets/6d5e9da0-56a8-4920-bf9c-61eef99a49cc)
  ![image](https://github.com/user-attachments/assets/8bcf09cd-edcc-43f6-b31c-e3e6b979cc97)
  ![image](https://github.com/user-attachments/assets/52a9e568-35fd-442f-90f1-50680d4644d9)
  ![image](https://github.com/user-attachments/assets/4bb0cd77-9e41-46c8-9f9f-02f84206bb4f)
  ![image](https://github.com/user-attachments/assets/09891f26-a1b6-4452-89b0-cc9d271c0e25)
  ![image](https://github.com/user-attachments/assets/314a9cf4-f52e-417e-b2d2-09f3b53b6961)
  - Chatbot Interface
  ![image](https://github.com/user-attachments/assets/adebb83e-75fd-4f01-a63c-57dd39e012eb)




