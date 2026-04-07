# Docker Exercise Evidence

## DockerHub Username
**Tu username de DockerHub debe ir aquí** (necesitas crear una cuenta en https://hub.docker.com si no tienes una)

## Command Evidence

### 1. Docker Desktop Installed and Running
```powershell
PS C:\Users\Gustavo\Desktop\node-docker-app> docker --version
Docker version 28.3.2, build 578ccf6

PS C:\Users\Gustavo\Desktop\node-docker-app> docker ps
CONTAINER ID   IMAGE             COMMAND                  CREATED         STATUS         PORTS                                         NAMES
99a53d9e88f7   node-docker-app   "docker-entrypoint.s…"   3 seconds ago   Up 2 seconds   0.0.0.0:3000->3000/tcp, [::]:3000->3000/tcp   node-docker-app-container
```

### 2. Building Docker Image
```powershell
PS C:\Users\Gustavo\Desktop\node-docker-app> docker build -t node-docker-app .
[+] Building 15.4s (11/11) FINISHED
 => [internal] load build definition from Dockerfile
 => [internal] load .dockerignore
 => [internal] load metadata for docker.io/library/node:18-alpine
 => [1/5] FROM docker.io/library/node:18-alpine
 => [2/5] WORKDIR /app
 => [3/5] COPY package*.json ./
 => [4/5] RUN npm install
 => [5/5] COPY . .
 => exporting to image
 => => writing image sha256:84391c7c34e7bc0d90104a67ca680ea466f878591895127a8358df8fbbdcc5ed
 => => naming to docker.io/library/node-docker-app:latest
```

### 3. Docker Images List
```powershell
PS C:\Users\Gustavo\Desktop\node-docker-app> docker images
REPOSITORY        TAG       IMAGE ID       CREATED          SIZE
node-docker-app   latest    84391c7c34e7   16 seconds ago   181MB
```

### 4. Running Container
```powershell
PS C:\Users\Gustavo\Desktop\node-docker-app> docker run -d -p 3000:3000 --name node-docker-app-container node-docker-app
99a53d9e88f72ec70ff138649e7a1b279aad372a2d3d6cd1cc883d81e3edf508
```

### 5. Testing Application
```powershell
PS C:\Users\Gustavo\Desktop\node-docker-app> curl http://localhost:3000
Hello, Docker!
```

## Screenshots Required
Please take screenshots of:
1. **Docker Desktop** - Showing it's installed and running
2. **Terminal/PowerShell** - With the commands visible and your Windows username visible
3. **Browser** - Open http://localhost:3000 showing "Hello, Docker!"

## DockerHub Username
Enter your DockerHub username here: `_________________`

## GitHub Repository
After pushing, the repository URL will be: `https://github.com/Tav07/node-docker-app`