## 3.Start Server
### Linux/Unix/Mac
Run the following command to sart(standalone means non-cluster mode):

> sh startup.sh -m standalone

If you are using a ubuntu system, or encounter this error message [[symbol not found, try running as follows:

> bash startup.sh -m standalone

### Windows
Run the following command to start:

> cmd startup.cmd

Or double-click the startup.cmd run file.

## 4.Service & Configuration Management
Service registration
> curl -X POST 'http://127.0.0.1:8848/nacos/v1/ns/instance?serviceName=nacos.naming.serviceName&ip=20.18.7.10&port=8080'

Service discovery
> curl -X GET 'http://127.0.0.1:8848/nacos/v1/ns/instance/list?serviceName=nacos.naming.serviceName'

Publish config
> curl -X POST "http://127.0.0.1:8848/nacos/v1/cs/configs?dataId=nacos.cfg.dataId&group=test&content=helloWorld"

Get config
> curl -X GET "http://127.0.0.1:8848/nacos/v1/cs/configs?dataId=nacos.cfg.dataId&group=test"

## 5.Shutdown Servers
Linux/Unix/Mac
> sh shutdown.sh

Windows
> cmd shutdown.cmd

> Or click the shutdown.cmd file operation.