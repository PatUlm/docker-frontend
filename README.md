## Start development

```
$ docker run -p 3000:3000 -v /app/node_modules -v $(pwd):/app dec7af926df7e32eb5f7082637a060343acab6d41dc709d8bf39859717c1bf12
```

## Start tests in development container

```
$ docker ps
$ docker exec -it 04cdafefe547 npm run test
```

## Start tests in CI pipeline

```
$ docker run -e CI=true pulmer75/docker-frontend npm run test
```

## Release

```
$ docker build .
$ docker run -p 8080:80 a76dcac2ac93356302490ec5ac5c898e27def64fc682df21f9c39ec0c9abb782
```
