# Pocketbase Docker Image

Open Source realtime backend in 1 docker image

📖 Official Documentation: [PocketBase Docs](https://pocketbase.io/docs/)

## 🚀 Getting Started

### Using Docker CLI

Run the following command to start PocketBase:

```bash
docker run \
    -p 8080:8080 \
    -v /path/to/data:/pb/pb_data \
    ctrlouis/pocketbase:latest
```
- -p 8080:8080: Maps the container's port 8080 to your host's port 8080.
- -v /path/to/data:/pb/pb_data: Mounts a volume to persist your database data.

Replace /path/to/data with the absolute path on your host machine where you want to store PocketBase data.

### Using Docker Compose

```
services:
    pocketbase:
        image: ctrlouis/pocketbase:latest
        ports:
            - "8080:8080"
        volumes:
            - pocketbase_data:/pb/pb_data

volumes:
    pocketbase_data:
```
Save and run with docker-compose up -d.
The pocketbase_data volume ensures your data persists across container restarts.

## 🛠 Building the Image Locally

To build and push your own version of the Docker image:

1. Build the image:
`docker build -t ctrlouis/pocketbase:latest .`
2. Push the image to Docker Hub:
`docker push ctrlouis/pocketbase:latest`

## 📚 Resources

- [PocketBase Official Website](https://pocketbase.io/)
- [PocketBase Documentation](https://pocketbase.io/docs/)
- [GitHub Repository](https://github.com/pocketbase/pocketbase)
