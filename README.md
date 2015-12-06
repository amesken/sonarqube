[![](https://badge.imagelayers.io/amesken/sonarqube:latest.svg)](https://imagelayers.io/?images=amesken/sonarqube:latest 'Get your own badge on imagelayers.io')

# SonarQube

Run [Sonarqube](http://www.sonarqube.org/) inside a Docker container.

(this image is using the embedded h2 database)

## Volumes
Sonarqube `data`, `logs` and `extensions` directories are exported as data volume:

    <USER_HOME>/docker/data/sonarqube/data
    <USER_HOME>/docker/data/sonarqube/logs
    <USER_HOME>/docker/data/sonarqube/extensions

## Ports
The service is exposed through port `9000`.

## Example
To run sonarqube do:

	docker run -p 19000:9000 amesken/sonarqube

Now point your browser to http://192.168.99.100:19000/sonar

Administration is done by user `admin` with password `admin`.

## Context of this image
This sonarqube image is originally created to work with a complete Continuous Delivery tool stack which can be obtained from [docker](https://hub.docker.com/r/amesken/cd-tool-stack/) or [github](https://github.com/amesken/cd-tool-stack).
The image is based on [this blog article](https://blog.codecentric.de/en/2015/10/continuous-integration-platform-using-docker-container-jenkins-sonarqube-nexus-gitlab) by Marcel Birkner.