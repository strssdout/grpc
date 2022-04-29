###

To generate proto files:

cd cars/

protoc cars.proto --go_out=. --go_opt=paths=source_relative --go-grpc_out=. --go-grpc_opt=paths=source_relative --proto_path=.

cd engines/

protoc engines.proto --go_out=. --go_opt=paths=source_relative --go-grpc_out=. --go-grpc_opt=paths=source_relative --proto_path=.

run 
```
protoc-go-inject-tag -input=./test.pb.go
```
to generate redis fields in EngineResponse struct