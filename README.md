# Maregraph docker examples


### Log members to file

```
# Build the container
docker build -t log-to-file -f Dockerfile-to-file .

# Touch the output
touch output.ttl

# Run the container
docker run -v $(pwd):/tmp/pipeline log-to-file /tmp/pipeline/pipeline.ttl
```


### Ingest dump into ldes

```
# get the dump
wget https://www.marineregions.org/export/MRGID-LDES-export.zip -O export.zip
unzip export.zip

# start docker compose
docker-compose up
```

