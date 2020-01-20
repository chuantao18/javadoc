final、finally、finalize的区别

final

1、把类或者方法声明为final，明确的告诉，这些行为不可以修改

```java
public final class String
    implements java.io.Serializable, Comparable<String>, CharSequence {
}
```

观察java.lang包下的一些类，很多都声明为final class。一些第三方类库也是如此，这可以有效避免 API 使用者更改基础功能，某种程度上，这是保证平台安全的必要手段。

2.使用final修饰参数或者变量，避免不必要的赋值错误

```java
    public void query(final String test) {
		//test = "abc";
        System.out.println(test);
    }
```

上面的方法里不可以再次对test参数赋值，注释代码编译时是报错的。

3.final 变量产生了某种程度的不可变（immutable）的效果，用于保护只读性数据。在并发编程中，因为明确地不能再赋值 final 变量，有利于减少额外的同步开销，也可以省去一些防御性拷贝的必要。

4.final不等同于immutable



​	