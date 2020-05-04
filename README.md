# drone-caddy-pipeline
A docker-compose configuration that runs a Drone server with a job runner. SSL is configured via a Caddy proxy. 

## Setup
Follow step 1 of the [Drone documentation](https://docs.drone.io/) to create an OAuth app and generate credentials. 

1) Ensure the .env file is set:
```
mv drone.env.example drone.env
```

2) Set the variables in `drone.env`.

3) Set the hostname in the `Caddyfile`.

4) Make sure port 443/8000 are exposed in your firewall.

5) Add the following line to your `/etc/hosts` file:
```
127.0.0.1 yyy.xxx.com
```

### :fire: Build the enviroment 
```
make up
```