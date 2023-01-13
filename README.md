# Docker-Quick-Help

## Totally Clean out Docker

**Stop all docker containers and apps and then remove them:**

~~~bash
docker ps -aq | xargs docker stop | xargs docker rm
~~~

**Remove all docker images:**

~~~bash
docker rmi $(docker images -a -q)
~~~

**Remove all docker volumes:**

~~~bash
docker volume rm $(docker volume ls -qf dangling=true)
~~~



##### Note:

The Linux command, ***xargs***, reads lines of text from the standard input or output of another command and then turns them into commands that are then executed.
