PROTO_FILES := $(shell find pkg -name "*.proto")

proto:
	protoc --go_out=. --go_opt=paths=source_relative \
		--go-grpc_out=require_unimplemented_servers=false:. --go-grpc_opt=paths=source_relative \
		$(PROTO_FILES)

server:
	go run cmd/main.go