## InitLogger 方法

**主要适用于Windows系统日志管理，可实现以下功能：** 

```
1、不同级别的日志输出到不同的日志文件中； 

2、日志文件可按照文件大小或日期进行切割存储，以避免单一日志文件过大； 

3、日志使用简单方便，一次定义全局使用。
```



**使用示例：**

```go
func main() {
    warnFile := "./log/warn/warn.log"
    infoFile := "./log/info/info.log"
    debugFile := "./log/cim.log"
    newName := "-%Y%m%d.log"
    maxSaveTime := time.Hour*24*30
    rotationTime := time.Hour*24

    InitLogger(warnFile, infoFile, debugFile, newName, maxSaveTime, rotationTime)
}
```