# Java中四种引用关系
在堆中产生一个数组或者一个对象后，可以在栈中定义一个特殊的变量指向这个数组/对象，这个变量的取值等于数组或对象在堆内存的**首地址**
## 强引用
- 最常见的引用， `A a = new A()`就是强引用
- GC永远不会回收强引用的对象

## 软引用
- 一般将有用但是非必需的对象声明为软引用
- 将要发生内存溢出之前，GC会把这些对象列进回收范围
- 用`SoftReference`类指向的对象

## 弱引用
- 将非必须对象声明为弱引用
- 弱引用对象只能生存到下次GC前（无论内存是否足够，下次GC一定会会回收弱引用对象）
- 用`WeakReference`类指向的对象

## 虚引用
- 一个对象是否有虚引用的存在，完全不会对其生存时间进行影响
- 这个对象在被回收时，可以收到一个系统通知
