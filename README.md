# To build and run
```
docker build -t my_image . && docker run -tid -v `{pwd}`/app:/usr/src/app -p 3000:3000 my_image
```
# To list the docker containers
```
docker ps
```
result:
```
CONTAINER ID   IMAGE      COMMAND                  CREATED         STATUS         PORTS                    NAMES
875d8e7c8830   my_image   "docker-entrypoint.s…"   2 minutes ago   Up 2 minutes   0.0.0.0:3000->3000/tcp   magical_lehmann
```
# To view the logs
```
docker logs -f <chainer_id>
// where <chainer_id> is 875 as this example
```
result:
```
Compiled successfully!

You can now view app in the browser.

  Local:            http://localhost:3000
  On Your Network:  http://172.17.0.2:3000

Note that the development build is not optimized.
To create a production build, use yarn build.
```
# surf the react-app page
```
http://localhost:3000
```
