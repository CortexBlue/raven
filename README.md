# Raven

A distributed task queue system built with Go, gRPC, and Kubernetes.

## Setup

1. Install protoc:
```bash
   brew install protobuf
```

2. Install Go protobuf tools:
```bash
   go install google.golang.org/protobuf/cmd/protoc-gen-go@latest
   go install google.golang.org/grpc/cmd/protoc-gen-go-grpc@latest
```

3. Generate protobuf code:
```bash
   protoc --go_out=. --go_opt=paths=source_relative \
          --go-grpc_out=. --go-grpc_opt=paths=source_relative \
          api/proto/task.proto
```
