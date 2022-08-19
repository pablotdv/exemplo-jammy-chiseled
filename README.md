docker build  -f Dockerfile.new . -t dotnetapp-nova --no-cache

docker build  -f Dockerfile . -t dotnetapp-atual --no-cache

docker run -d -p 8080:80 --name dotnetapp-atual dotnetapp-atual

docker run -d -p 8081:8080 --name dotnetapp-nova dotnetapp-nova