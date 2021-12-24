## Docker
```
docker-compose up --build --remove-orphans --force-recreate
```

#### Parando o ambiente sem destruir o banco:
```
docker-compose down 
```

#### Parando o ambiente destruindo o banco:
```
docker-compose down --volumes 
```

#### Stop all running containers
```
docker stop $(docker ps -a -q)
```

#### Delete all stopped containers
```
docker rm $(docker ps -a -q)
```

## CONFIG WINDOWS MEMORY

### turn off all wsl instances such as docker-desktop

#### Config vmmem
```
wsl --shutdown
notepad "$env:USERPROFILE/.wslconfig"
```

#### Set the values you want for CPU core and Memory:
```
memory=3GB   # Limits VM memory in WSL 2 up to 3GB
processors=2 # Makes the WSL 2 VM use two virtual processors
```