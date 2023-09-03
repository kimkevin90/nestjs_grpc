1. initial package install
- nest new nestjs-grpc

2. using mono repo
- nest generate app auth

3. setting for grpc in auth repo
- nest g resource users

4. convert proto to ts
- protoc --plugin=./node_modules/.bin/protoc-gen-ts_proto --ts_proto_out=./ --ts_proto_opt=nestJs=true ./proto/auth.proto

5. create common lib
- nest g lib common