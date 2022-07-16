# milvus-sdk-csharp

![](./milvussharp.png)

C# SDK for Milvus.

## Getting Started

### Prerequisites

What things you need to install the software and how to install them

```
.net framework 4.6.1 or higher
.net 5.0 or .net 6.0
```

### Installing

```
Install-Package IO.Milvus -Version 2.0.0-alpha
```

### Examples

Connect client

```csharp
var milvusClient = new MilvusServiceClient(
    ConnectParam.Create(
    host: "192.168.100.139",
    port: 19531));
```
disconnet

```csharp
milvusClient.close();
```

Please refer to [Test Project](https://github.com/weianweigan/milvus-sdk-csharp/tree/develop/src/IO.MilvusTests) for more examples.

### Grpc client

You can find code auto generated by grpc tools in IO.Milvus.Grpc and use auto-generated serviceclient to connect server.
```csharp
var defualtClient = MilvusServiceClient.CreateGrpcDefaultClient(
    ConnectParam.Create(
        host: "192.168.100.139",
        port: 19531));
```