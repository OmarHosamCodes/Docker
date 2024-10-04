# Use an official Go image with the correct version
FROM golang:1.23-alpine

# Set the working directory inside the container
WORKDIR /app

RUN apk --no-cache add curl neofetch

RUN curl -L https://github.com/danielmiessler/fabric/releases/latest/download/fabric-linux-arm64 > fabric && \
    chmod +x fabric

# Set environment variables for Go paths
ENV GOROOT=/usr/local/go
ENV GOPATH=/root/go
ENV PATH=$GOPATH/bin:$GOROOT/bin:/root/.local/bin:/usr/local/bin:/usr/bin:/bin

# Set the default command to run Fabric
CMD neofetch
