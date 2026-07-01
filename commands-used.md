# Commands Used

## Check Java Version

```cmd
java -version
```

## Check Docker Version

```cmd
docker --version
```

## Run OWASP Juice Shop

```cmd
docker run -d --name juice-shop -p 3000:3000 bkimminich/juice-shop
```

## Check Running Containers

```cmd
docker ps
```

## Stop Juice Shop

```cmd
docker stop juice-shop
```

## Start Juice Shop Again

```cmd
docker start juice-shop
```

## Remove Juice Shop Container

```cmd
docker rm juice-shop
```
