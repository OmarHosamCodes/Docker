# Use an official Go image with the correct version
FROM golang:1.23-alpine

# Set the working directory inside the container
WORKDIR /app

RUN apk --no-cache add curl

# Set environment variables for Go paths
ENV GOROOT=/usr/local/go
ENV GOPATH=/root/go
ENV PATH=$GOPATH/bin:$GOROOT/bin:/root/.local/bin:/usr/local/bin:/usr/bin:/bin

RUN go install github.com/danielmiessler/fabric@latest

# Set the default command to run Fabric
CMD ["fabric", "--setup"]
