# Simple Nginx Website with Docker

This project demonstrates how to containerize a static HTML website using Docker and serve it using the Nginx web server.


## 🚀 How to Run

### 1. Ensure Docker is Installed
Make sure Docker is installed and running on your system.  
👉 Download it from [https://www.docker.com/products/docker-desktop](https://www.docker.com/products/docker-desktop)

### 2. Navigate to the Project Directory
Open a terminal and go to the directory containing this `README.md`, the `Dockerfile`, and the `static-web/` folder.

```bash
cd /path/to/project-directory
```
### 3. Build the Docker Image

This command builds the image based on the Dockerfile. The -t flag tags the image with a name (nginx-webapp):
```
docker build -t nginx-webapp .
```
### 4. Run the Container

This command creates and starts a container from the image:

```
docker run -d --name ashish-nginx -p 5000:80 nginx-webapp:latest

```
- -d runs the container in "detached" mode (in the background).

- --name ashish-nginx gives the container a friendly name.

- -p 5000:80 maps port 5000 on your host machine to port 80 inside the container.

- nginx-webapp:latest specifies the image to use.
### 5. View Your Website

Open your web browser and navigate to:
```
http://localhost:5000
```

You should see your static website being served by Nginx! 🎉

---

## 🛠️ Common Docker Commands

| Task                   | Command                          |
|------------------------|----------------------------------|
| Check running containers | `docker ps`                    |
| Stop the container       | `docker stop ashish-nginx`     |
| Remove the container     | `docker rm ashish-nginx`       |
| View container logs      | `docker logs ashish-nginx`     |

---

## 📌 Notes

- Ensure port `5000` is not in use before running the container.
- You can change the port mapping by modifying the `-p` option, for example:  
  ```bash
  docker run -d --name ashish-nginx -p 8080:80 nginx-webapp:latest

