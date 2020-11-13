# with语法

#### 知识点：

- with



#### 代码示例：

```kotlin
class Mysql{

    fun connect(){
        println("Mysql数据库连接")
    }

    fun update(){
        println("Mysql数据库更新")
    }

    fun close(){
        println("Mysql数据库连接关闭")
    }
}

fun main() {
    // 实例化Mysql
    val mysql = Mysql()
    
    // with 调用方法
    with(mysql){
        connect()
        update()
        connect()
    }
}
```

