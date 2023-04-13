This is a Dockerfile to locally run a tiny NGINX website in a container.
So start off by cloning the repository however you usually do. 
Or. 
Using CLI: 
```
git clone -b master https://github.com/ttothewiggy/Ubuntu-Dockerfile.git
```

Check docker is running ny running 
```
docker info
```

Navigate in the CLI to the folder from github "Ubuntu-Dockerfile" and run: 
```
docker build .
```

Once built, you should be able to see the image without a name usinf:
```
docker images
```

If you want to name the image run: 
```
dockerbuild -t <image-name> .
```

Execute the image to create the container by running: 
```
docker run -d -p 80:80 051bcf7b3c09
```
(The last set of numbers starting "051" is the image ID you take from the image when you run the "docker images" command.)

Using 
```
docker ps
```
we should see the container running. 

To get running on Mac, I used this command to specify the build.

```
docker buildx build --platform linux/arm64 -t my-image .
```
```
docker stop <image_name>
```
Stops the container