JVM 调优

JVM 包含 classLoader，java类库，字节码解释器和即时编译器(JIT)

JDK 包含JRE 包含JVM

HotSpot是实现JVM的一种

类加载
类加载分为 loading linking 和 initializing三步，其中linking又分为verification，preparation和resolution三步。
preparation 将class里的静态变量赋默认值，resolution将class中常量池中的符号引用转变成为内存地址。
initialzing将静态变量默认值赋为初始值。

类加载器 classloader
bootstrap  加载lib目录下的核心类 C++实现
Extension  加载ext目录下的扩展包
App        加载classpath指定内容
CustomClassLoader  自定义classloader

类加载过程：双亲委派机制