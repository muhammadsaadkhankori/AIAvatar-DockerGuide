# Interactive Avatar AI - Docker Setup

Welcome to the **Interactive Avatar AI** project! This repository contains everything you need to easily deploy and run the Interactive Avatar AI project using Docker, which includes both the frontend and backend services.

## **Table of Contents**
1. Overview
2. Prerequisites
3. Installation
4. Running the Application
5. Accessing the Application
6. Stopping the Application
7. Troubleshooting
8. Contributing
9. License

---

## **Overview**

This project provides a Dockerized environment for the Interactive Avatar AI, which includes a frontend (powered by Vite and React) and a backend (powered by Node.js). Using Docker, you can run the entire project with ease by following the steps below.

## **Prerequisites**

Before running the application, ensure that your system meets the following requirements:

- Docker: You need to have Docker installed on your machine. You can download and install Docker from the official website at [Get Docker](https://www.docker.com/get-started).
- Docker Compose: This tool comes with Docker Desktop, so make sure it’s available on your machine. You can learn more about it at [Docker Compose](https://docs.docker.com/compose/).

---

## **Installation**

To begin:

1. First, clone this repository to your local machine. You can do this by running the following command in your terminal:

   `git clone https://github.com/<your-github-username>/InteractiveAvatarAI-Docker.git`

2. Navigate into the project directory:

   `cd InteractiveAvatarAI-Docker`

3. Next, log in to Docker Hub to ensure you can pull the necessary images. Run the following command:

   `docker login`

   If you don’t have a Docker Hub account, you can create one [here](https://hub.docker.com/).

---

## **Running the Application**

1. To start the application, ensure you have the latest Docker images by pulling them with the following command:

   `docker-compose pull`

2. Once the images are pulled, you can start both the frontend and backend services by running:

   `docker-compose up`

3. If you prefer to run the application in the background (detached mode), you can use:

   `docker-compose up -d`

This will start the services, and you’ll be able to access the application as described below.

---

## **Accessing the Application**

Once the application is running, you can access the following services in your browser:

- **Frontend**: Access the user interface at [http://localhost:5173](http://localhost:5173).
- **Backend (if applicable)**: Access the backend API at [http://localhost:3000](http://localhost:3000).

---

## **Stopping the Application**

To stop the running containers and remove them, you can run:

`docker-compose down`

This will shut down all services and remove any associated networks.

---

## **Troubleshooting**

Here are some common issues and their solutions:

1. **Issue**: Docker containers fail to start.
   - **Solution**: Ensure Docker is running and the necessary images are pulled. You can do this by running `docker-compose pull` to fetch the latest images.

2. **Issue**: Port is already in use.
   - **Solution**: Make sure no other services are running on port `5173` (for the frontend) or `3000` (for the backend). If needed, stop conflicting services or change the port in the `docker-compose.yml` file.

3. **Issue**: Cannot connect to Docker Hub.
   - **Solution**: Make sure you're logged in to Docker Hub by running `docker login`.

4. **Issue**: Backend service not responding.
   - **Solution**: Ensure that both the frontend and backend services are running, and check the logs for errors using `docker-compose logs`.

---

## **Contributing**

We welcome contributions! To contribute to the project:

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Commit your changes.
4. Push to your branch.
5. Submit a pull request for review.

---

## **License**

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

### **Notes for Users**

- **Docker Compose** simplifies the process of pulling, building, and running the images. You should use the command `docker-compose up` to start the services.
- If you encounter any issues, you can view the logs of the services by running `docker-compose logs`.

Let us know if you experience any problems by opening an issue in this repository!
