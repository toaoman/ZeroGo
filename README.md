# ZeroNet Golang client

Very basic ZeroNet client implementation.

## Usage

* Just run it and wait for new browser tab openning

## TODO for next version

- [ ] Bugfixes
- [ ] Optimization of system resources and bandwidth utilization
- [ ] SQLite support
- [ ] Site update process


golang的版本为1.10

使用go get -u -v github.com/G1itchZero/ZeroGo  
拖至本地GOPATH中测试。[注意在windows下要挂sstap全局代理]
下载后进入"GOPATH"\src\github.com\G1itchZero\ZeroGo\
运行 go run main.go 测试。
报错src\github.com\G1itchZero\ZeroGo\server\server.go:92:3: e.Color undefined (type*echo.Echo has no field or method Color)

对此报错，进入src\github.com\G1itchZero\ZeroGo\server\server.go文件中把第92行“e.Color.SetOutput(ioutil.Discard)”用“//"注释掉即可。

修改保存后重新运行go build就会在ZeroGo目录中生成ZeroGo.exe
运行后就会打开浏览器进入zeronet了。

在“src\github.com\G1itchZero\ZeroGo\utils\utils.go”的第165行到170行是编译进程序里的tracker服务器地址，这里可以添加新的tracker服务器地址再进行编译。

另外在运行编译之中可能需要gcc，参考"https://www.cnblogs.com/zsy/p/5958170.html"中的方法去
https://sourceforge.net/projects/mingw-w64/files/
下载“mingw-w64-install.exe”安装即可。

这个golang编写的简单的zeronet的客户端目前打开网页时有显示不完整的情况，原因未明，但应该是能连上zeronet网络。
