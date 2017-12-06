# ezmaster-web-term

[![Docker Pulls](https://img.shields.io/docker/pulls/inistcnrs/ezmaster-web-term.svg)](https://registry.hub.docker.com/u/inistcnrs/ezmaster-web-term/)

Web terminal used for debugging [ezmaster](https://github.com/Inist-CNRS/ezmaster) stuff.

## Usage

- Add the application in your [ezmaster](https://github.com/Inist-CNRS/ezmaster) ([inistcnrs/ezmaster-web-term:1.0.2](https://hub.docker.com/r/inistcnrs/ezmaster-web-term/tags/)) then create a new instance
- Open your browser, click on the instance web url and enjoy

### Usage for ezmaster's mongodb cleanup

```shell
apt update
apt install mongodb-clients
mongo --host ezmaster

> show databases
...
> use my-ezvis-1;
> db.dropDatabase();
```

It could be usefull to cleanup old ezvis databases stored in the mongo ``ezmaster_db`` database.

## Developer

To run stuff locally, just type:

```
make build
docker run -it --name ezmaster-web-term --rm -p 8080:80 inistcnrs/ezmaster-web-term:1.0.2
```

Then open your browser on http://localhost:8080
