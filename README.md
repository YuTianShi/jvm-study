# jvm-study

![](pic/image1.png)

## 方法执行过程

- jvm申请内存
  
- 初始化运行时数据区
  
  方法区：存放 class；静态变量：常量
  
  堆：实例对象
  
  栈：栈帧（对象的引用，方法）
  
- 类加载
  
- 执行方法
  
- 创建对象
  

## 堆空间分代划分
![](pic/image.png)
## outOfMemory异常

![](pic\image2.jpg)

```
https://docs.oracle.com/javase/8/docs/technotes/tools/unix/java.html
可以看jvm参数查看网址
```

- [ ] Direct buffer memory ： 直接内存太大（-XX:MaxDirectMemorySize=100m）
  
- [ ] Java heap space： 堆内存溢出 （-Xms30m -Xmx30m -XX:+PrintGCDetails）
  
- [ ] GC overhead limit exceeded： gc占用98%的资源回收效率不足2%的（-Xms30m -Xmx30m）
  
- [ ] Metaspace：方法区异常----（XX:MetaspaceSize=10M -XX:MaxMetaspaceSize=10M）
  

# 常量池（方法区）

1. class常量池
  
  - class的方法
    
  - 字面量（String a = "b"）
    
  - 符合引用，类加载过程中根据符合引用变为直接引用
    
2. 运行时常量池 ---虚拟机规范定义的
  
  直接引用放到运行时常量池
  
3. 字符串常量池
  
  专门针对String的
