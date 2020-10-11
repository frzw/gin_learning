# 三大问题
1. gin是什么？
- 用go编写的web框架，高性能、高效率。
    - httprouter:轻质高性能的HTTP请求路由器;针对高性能和较小的内存占用进行了优化。
- 特点：
    - 快速：Radix树路由
        - Radix树：基数树;key-value存储查找;插入、删除、查询操作复杂度为O(n);空间优化，只有一个子节点的中间节点将被压缩。
    - 支持中间件: HTTP请求可以由中间件和最终操作来处理。
    - Crash处理: panic恢复，服务器始终可用。
    - JSON验证: 
    - 路由组：
    - 错误管理：
    - 内置渲染：
    - 可扩展性：

2. gin能做什么？
    - 利用其提供的api可以进行web开发。
        - web开发：客户端/服务器模型，客户端由前端编写，服务器由后端编写，后端提供数据给前端，前端拿到数据进行展示，前后端的通信通过接口进行通信（resful、graphql）

3. gin怎么使用？
- 下载安装gin包
    - go get -u github.com/gin-gonic/gin
- import导入
    - import "github.com/gin-gonic/gin"
- 编写test.go代码
    ```
    func main(){
        r := gin.Default
        r.GET("/test", func(c *gin.Context){
            c.JSON(200, gin.H{
                "message":"testing",
            })
        })
        r.Run(":8080")
    }

    ```
- 运行test.go   
    - go run test.go