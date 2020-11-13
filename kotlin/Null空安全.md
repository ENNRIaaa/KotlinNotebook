# Null空安全

#### 知识点：

- null
- null允许符号：?
- 跳过编译时null检测：!!



#### 代码示例：

```kotlin
fun main() {

    // 编译报错（null空安全特性）
    var name: String
    //name = null

    // 数据类型后加?  表示允许为null
    var title: String?
    title = "我的文章"

    if (title != null) {
        println("$title")
    }

    var length = title.length
    println("length is $length")

    title = null
    // title虽然允许为null，但是调用属性时会出现编译错误
    // val length1 = title.length

    // !!表示非空断言，断言title不为空，但是会出现运行时错误
    val length1 = title!!.length
    println("length is $length1")
}
```

