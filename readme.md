go get -u google.golang.org/grpc
go get -u github.com/golang/protobuf/protoc-gen-go
protoc-3.14.0-x86_64

gRPC开发分三步：

1.编写.proto文件，生成指定语言源代码。
helloworld.proto
protoc -I helloworld/ helloworld/pb/helloworld.proto --go_out=plugins=grpc:helloworld
2.编写服务端代码(业务实现逻辑在服务端编写)
server.go
3.编写客户端代码
client.go