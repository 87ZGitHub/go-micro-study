build:
# 一定要注意 Makefile 中的缩进，否则 make build 可能报错 Nothing to be done for build
# protoc 命令前边是一个 Tab，不是四个或八个空格
	# protoc -I. --go_out=plugins=micro:$(GOPATH)/src/shippy/consignment-service \
	# 	proto/consignment/consignment.proto
	GOOS=linux GOARCH=amd64 go build
    docker build -t consignment-service .
run: 
    docker run -p 50051:50051 consignment-service
