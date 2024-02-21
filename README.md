# Vliz docker examples


### Log members to file

```
# Build the container
docker build -t log-to-file -f Dockerfile-to-file .

# Touch the output
touch output.ttl

# Run the container
docker run -v $(pwd):/tmp/pipeline log-to-file /tmp/pipeline/pipeline.ttl
```

