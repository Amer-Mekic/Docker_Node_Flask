# Dockerized Node.js and Python Applications

This repository contains Docker configurations for two applications:

- **A Node.js application** (runs on port `3000`)
- **A Python application** (runs on port `5000`)

Each app is containerized using its respective `Dockerfile`.

---

## Prerequisites

Ensure you have the following installed:

- [Docker](https://www.docker.com/)
- (Optional) [Docker Compose](https://docs.docker.com/compose/) — if you want to manage both containers together

---

## Building and Running the Node.js App

### Location

The Dockerfile for the Node.js app is configured to:

- Use the official **Node.js 22** image
- Install dependencies from `package.json`
- Expose port `3000`
- Start the app using `npm start`

### Build the Image
```bash
docker build -t my-node-app -f Dockerfile.node .
```

# Running Dockerized Applications

## Run the Node.js Container
```bash
docker run -p 3000:3000 my-node-app
```

## Building and Running the Python App

The Dockerfile for the Python app:

- Uses the official Python 3 image
- Installs dependencies from requirements.txt
- Exposes port 5000
- Runs app.py as the entry point

# Build the Image
```bash
docker build -t my-python-app -f Dockerfile.python .
```

# Run the Container
```bash
docker run -p 5000:5000 my-python-app
```

# Stopping Containers:

Use docker ps to find the container ID, then stop with:
```bash
docker stop <container_id>
```