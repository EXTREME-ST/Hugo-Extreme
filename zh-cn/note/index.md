# JAVASE 基础知识笔记


# JAVA

[TOC]

## java 基础

### 基础语法

if……else……	if 选择结构

switch……case……break……default	switch 判断结构

while……	while 循环

do……while	do while 循环

for……	for 循环

continue	跳过循环

break	退出循环

return    退出当前方法，并返回值

编译类型[] 名字=new 运行类型[多少个数值]	创建数组

条件表达式？结果1：结果2	三元运算符

```java
Scanner 类名=new Scanner(System.in) //设置接收输入类
nextInt()	//接收数值
nextLine()	//接收所有
next()	//接收字符
```

```java
hashCode()	//返回哈希值
getClass()	//返回一个Class对象
```

```
UUID 方法
	randomUUID()		//返回一个唯一的字符串
```

```
System 常用方法
	System.exit()	//退出当前程序
	System.currentTimeMillis()	//返回当前时间距离1970-1-1的毫秒数
	System.gc()	//运行垃圾回收机制
    System.out.println() //将输入的值输出至控制台,并换行
    System.out.print() //将输入的值输出至控制台
    System.in	//获取键盘输入
```



### 数据类型

Random		此类的一个实例用于生成伪随机数流

MessageDigest		为应用程序提供消息摘要算法的功能



```
Random 子类:
	ThreadLocalRandom		//提供线程间独立的随机序列
	SplittableRandom		//非线程安全,但可以 fork 的随机序列实现
```



```java
int	//范围	-2147483648~2147483647
String	//字符串
double	//范围	+/-1.8E+308 (15 个有效位）
char	//单个字符
boolean	//true 或 false
byte	//范围	-128~127
short	//范围	-32768~32767
long	//范围	-9223372036854775808L~9223372036854775807L
    
Boolean	//对应 boolean
Character	//对应 char
Byte	//对应 byte
Short	//对应 short
Integer	//对应 int
Long	//对应 long
Float	//对应 float
Double	//对应 double
    
StringBuffer	//存放在堆中的 char 数组,用于替换 String
StringBuilder	//同上,没有 synchronized 关键字,线程不安全

BigInteger	//保存很大整数的类，只能用方法来进行计算
BigDecimal	//保存精度很高的小数，同上
```



```java
String 常用方法：
	length()	//获取字符串或数组的长度
	equals()	//对比字符,括号中填对比谁
	equalslgnoreCase()	//无视大小写对比字符
	charAt()	//提取字符串的单个字符
	indexOf()	//返回指定字符在字符串中第一次出现处的索引,没有返回-1
	trim()		//删除字符串的头尾空白符
	lastIndexOf()	//返回指定字符在此字符串中最后一次出现处的索引,没有返回-1
    substring()		//提取字符串的多个字符
	split()		//以设定的正则表达式为间隔获取字符串为数组
	toUpperCase()	//转成大写
	toLowerCase()	//转成小写
    compareTo()		//字符串比大小,大于返回大于0的数,小于返回小于0的数
	concat()	//将指定的字符串参数连接到字符串上
    contains()	//判断字符串中是否包含指定的字符或字符串,返回布尔类型
	toCharArray()	//将字符串转换为字符数组
    getBytes()		//将字符串转换为字节数组
    replaceAll("参数1","参数2")		//将正则表达式匹配到的字符串全部替换为指定字符串,参数1填正则表达式,参数2填替换的字符串
    matches("参数1")	//判断是否与参数1的正则表达式匹配,返回boolean
    join( CharSequence CharSequence...)		//使用指定分隔符将任意字符串拼接成一个
    chars()		//从字符串所有字符创建数据流
```

```java
StringBuffer、StringBuilder常用方法：
	append()	//将指定的字符串追加到此字符序列
	delete(1,1)	//删除指定索引范围的字符串,左闭右开
	replace(1,1,"nm")	//替换指定索引范围的字符
	indexOf()	//返回指定字符在字符串中第一次出现处的索引,没有返回-1
	insert(1,"nm")	//指定索引位置插入字符串
    setCharAt(int i ,char c)	//将第 i 个代码单元设置为 c
```

```java
数值方法:	
	Math.abs()	//返回绝对值
	Math.pow(1,几次方)	//返回次方
	Math.ceil()	//返回大于等于该数的整数
	Math.floor()	//返回小于等于该数的整数
	Math.round()	//返回四舍五入后的整数
	Math.sqrt()	//返回开方后的数
	Math.random()	//返回小于1大于等于零的随机数
    Math.max()	//返回两个参数中最大的那个
```

```java
数组方法:	
	Arrays.toString()	//遍历输出传入的数组
	Arrays.copyOf(数组名，拷贝多少)	//返回数组指定元素
	Arrays.fill(填充谁，填充什么)	//填充数组
	Arrays.equals(数组名，数组名)		//比较两个数组的内容是否完全相等
	Arrays.asList()	//将一组数值转换为 list
	Arrays.PI	//表示(Π/派)的常量
```

```java
Character 常用方法:
	isDigit()	//是否为数字
	isLetter()	//是否为字母
	isUpperCase()	//是否大写
	isLowerCase()	//是否小写
	isWhitespace()	//是否空格
	toUpperCase()	//转成大写
	toLowerCase()	//转成小写
```

```java
BigInteger 和 BigDecimal 计算方法:
    add()	//加
	subtract()	//减
	multiply()	//乘
	divide()	//除
```

```java
包装类常用方法：	
	.parse...()		//将String类型数据转换成对应类型数据,后缀根据不同包装类转换
```

```
Random 方法:
	doubles()		//返回一个有效的无限伪随机双值流,每个值介于零（含）和一（不含）之间
	ints()		//返回一个有效的无限伪随机整型值流
		...( int int ):每个值都符合给定的原点（包括）和界限（不包括）
	nextGaussian()		//返回此随机数生成器序列的下一个伪随机
```



1.String 在创建时可以传入 char 数组,并指定读取多少,语法为 new String(数组名,开始索引,结束索引)



### 特殊符号



```java
运算符:
    +	//加
    -	//减
    *	//乘
    /	//除
    %	//取余
    ++	//加1
    --	//减1
    ==	//等于
    !=	//不等于
    >	//大于
    <	//小于
    >=	//大于或等于
    <=	//小于或等于
    &&	//并且
    ||	//或者
    ！	//否
```

```java
占位符:
    %s	//用字符串替代
    %d	//用整数替代
    %.(保留多少小数)f	//用小数替代
    %c	//用 char 替代
```



### 面向对象

设置类：

```java
class    //创建类
interface    //创建接口类
enum	//创建枚举类
```

this    指向当前对象属性
super    指向当前父类属性

package    将文件打包

import    导入包

extends    继承类

implements    实现接口

instanceOf    判断对象运行类型

{……}    代码块



```
Enum 方法
	name	//返回当前对象名
	ordinal	//返回当前对象在类中的创建名次,从0开始
	values	//返回类中所有常量,数组形式
	compareTo	//比较两个常量的编号
```

访问修饰符类型：

```java
public    //公用，都能访问
protected    //受保护，只能被所在包或不同包的子类访问
默认    //只能被所在包访问
private    //只能被其所在的类访问
```

其他修饰符：

```java
static    //设置静态
final    //固定状态
abstract    //设置抽象
default		//在接口中实现方法
transient 	//让属性不被序列化
strictfp	//将运算指定为自带标准
```

for(接收变量 : 数组、集合名)	增强 for 循环



1. 方法从最底层调用，属性从近处获取
2. 子类可以调用父类的属性
3. 子类需要实现父类的抽象方法
4. 子类创建需要先使用父类的构造器
5. 类加载顺序：静态>继承关系>普通>构造器
6. 在形参的数据类型后面加上 ... 可传入多个相同数据类型的值,形参会根据传入的值变成相应的数组
7. 没有返回值属性的方法就是构造器，构造器的名字需要和类名一致，设定构造器可以在定义对象时设定好属性
8. 创建构造器会顶替默认的空白构造器
9. 有 static 的属性被所有对象共享,方法直接使用
10. 执行构造器时会优先执行一次代码块,加了 static 之后只会在类加载时使用一次
11. 加了 final 方法不能被重写,变量不能被更改,类不能被继承,和 static 一起使用时,调用此属性不会加载类
12. 使用 abstract 被重写的父类方法不用设置执行代码,抽象类才支持抽象方法,抽象类不能实例化,继承抽象类的类需要重写抽象类里的所有抽象方法
13. 接口类的方法默认拥有 abstract 和 public,接口不能实例化,接口属性只能是 public static final 修饰符,接口类只能继承接口类,可以实现多个接口,继承类和实现接口不冲突
14. 枚举类直接创建常量,语法为:常量名(实参), enum 类的构造器为私有，类为 final ,默认继承 Enum 类
15. 传参的时候可以传个类,语法为:new 编译类型(){//类属性},也可以用变量存
16. instanceOf 判断左边类是否实现了右边类
17. 接口中的 static 方法只能使用接口名调用
18. 想调用接口中的 default 方法需要在接口名后指定 super 属性



### SPI

ServiceLoader		服务提供者加载工具



```
ServiceLoader 方法:
	load( Class )		//创建一个新的服务加载器
	iterator()		//延迟加载此加载程序服务的可用提供程序
```



1. ServiceLoader 通过查找程序中 META-INF/services/ 中的文件来进行模块的注入
2. 文件的命名为实现的服务的全类名,内容为实现类的全类名,文件名不带后缀,实现类可以有多个



## java 进阶



### 注解

AnnotatedElement 		表示当前在此 VM 中运行的程序的注释元素,该接口允许以反射方式读取注释

Annotation		所有注解类型扩展的通用接口



```
Java自带的标准注解:
    @Deprecated		//表示代码被弃用，如果使用了被@Deprecated注解的代码则编译器将发出警告
    @Override		//表示当前的方法定义将覆盖父类中的方法
    @SuppressWarnings		//表示关闭编译器警告信息
    	all:抑制所有警告
```

```
元注解:
	@Retention		//标明注解被保留的阶段
		RetentionPolicy:注释保留策略
			SOURCE		//源文件保留
			CLASS		//编译期保留，默认值
			RUNTIME		//运行期保留，可通过反射去获取注解信息
	
	@Target		//标明注解使用的范围
		ElementType: Java 程序中的句法位置的简单分类
			TYPE		//类、接口、枚举类
			FIELD		//成员变量(包括：枚举常量)
			METHOD		//成员方法
			PARAMETER		//方法参数
			CONSTRUCTOR		//构造方法
			LOCAL_VARIABLE		//局部变量
			ANNOTATION_TYPE		//注解类
			PACKAGE		//可用于修饰:包
			
			JDK 1.8 新增:
				TYPE_PARAMETER		//类型参数
				TYPE_USE		//使用类型的任何地方
			
	@Inherited		//标明注解可继承
	@Documented		//描述在使用 javadoc 工具为类生成帮助文档时是否要保留其注解信息
```

```
JDK 1.8 新增元注解:
	重复注解:
        @Repeatable		//指示它注释其声明的注释类型是可重复的
    类型注解:
        @NonNull		//如果此类型对应的对象为空将报错
```

```
AnnotatedElement 的常用方法:
	isAnnotationPresent( Class )		//如果此元素上存在指定类型的注释，则返回 true，否则返回 false
		Class:注解类型对应的Class对象
		
	getAnnotation( Class<T> )		//如果存在这样的注释，则返回此元素的指定类型的注释，否则返回 null
		Class:同上
		<T>:要查询并返回的注解类型（如果存在）
		
	getAnnotations()		//返回此元素上存在的注释。如果此元素上没有注释，则返回值为长度为 0 的数组
	
	getAnnotationsByType( Class<T> )		//返回与此元素关联的注释,如果没有与此元素关联的注释,则返回长度为 0 的数组
		
	getDeclaredAnnotation( Class<T> )		//如果直接存在这样的注释,则返回此元素的指定类型的注释,否则返回 null,此方法忽略继承的注释
		
	getDeclaredAnnotationsByType( Class<T> )		//同上,如果没有直接或间接存在指定的注解,则返回长度为 0 的数组
	
	getDeclaredAnnotations()		//返回此元素上直接存在的注释,此方法忽略继承的注释
```



1. AnnotatedElement 是 Class , Method , Constructor 的父接口
2. 类型注解是标识对象类型的注解,只要是在类型的前面就都可以标
3. @Repeatable的值表示可重复注释类型的包含注释类型



### 异常处理

Exception		异常的基类

RuntimeException		运行时异常

IOException		IO异常



throws		声明一个异常，告知方法调用者

throw 		抛出一个异常，至于该异常被捕获还是继续抛出都与它无关



```java
RuntimeException 实现类:

	NullPointerException		//空指针异常
    NumberFormatException		//数字格式不正确异常
    NegativeArraySizeException		//数组长度为负异常
        
	ArrayIndexOutOfBoundsException		//数组下标越界异常
	ArithmeticException		//数学运算异常
    ArrayStoreException		//数组中包含不兼容的值抛出的异常
        
    ClassNotFoundException		//找不到类
	ClassCastException		//类型转换异常

    SecurityException		//安全性异常
        
    IllegalArgumentException		//非法参数异常
    IllegalStateException		//方法在非法或不适当的时间被调用
        
    ConcurrentModificationException		//在禁止并发修改的情况下，对象检测到并发修改
        
    UnsupportedOperationException		//对象不支持请求的方法
```

```
IOException 的实现类:
	IOException		//操作输入流和输出流时可能出现的异常
	EOFException		//文件已结束异常
	FileNotFoundException		//文件未找到异常
```



```java
异常处理语法：
    //捕获多个异常类型，并对不同类型的异常做出不同的处理
        try-catch		
        try-catch-finally
        try-finally 
            
try-with-resource 语法:
	//此语法会在最后将 () 中定义的资源关闭

	try ( 
        //需要关闭的资源对象,多个资源对象用 ; 分隔
    ) {
        
    } catch (FileNotFoundException e) {
        
    }

//注意:自动关闭是调用 AutoCloseable 接口的 close() 来实现自动关闭,所以资源必须实现了 AutoCloseable 接口
```



1. 同一个 catch 也可以捕获多种类型异常，用 | 隔开

2. 当 try 没有捕获到异常时, try 语句块中的语句逐一被执行,程序将跳过catch语句块,执行 finally 语句块和其后的语句

3. 当 try 语句块里的某条语句出现异常时,而没有处理此异常的 catch 语句块时,此异常将会抛给 JVM 处理, finally 语句块里的语句还是会被执行，但 finally 语句块后的语句不会被执行

4. catch 语句块执行完后,执行 finally 语句块里的语句,最后执行 finally 语句块后的语句

5. try、catch 和 finally 都不能单独使用，只能是 try-catch、try-finally 或者 try-catch-finally

6. try 语句块监控代码，出现异常就停止执行下面的代码，然后将异常移交给 catch 语句块来处理

7. finally 语句块中的代码一定会被执行，常用于回收资源

   

### 集合

Iterator		迭代器

Map		双列集合

Collection		单列集合

Iterator		迭代器



```
双列集合实现类:
	HashMap		//哈希表
	TreeMap 	//有序哈希表
	Hashtable 	//哈希表，线程安全
    	Properties:专门读取配置文件的集合
            load()		//将IO流赋给 Properties 集合
            list()		//将k-v显示出来,比如 System.out 显示在控制台
            getProperty()		//根据输入的键获取值
            setProperty()		//添加k-v
            store(IO,注解)		//将添加的k-v保存在指定IO流,注解可以为null
	ConcurrentHashMap		//采用分段同步的哈希表
            
	WeakHashMap		//使用弱引用的表
```

```
单列集合实现类:
	List		//根据插入顺序排序
    	ArrayList:数组格式
            ensureCapacity( int )		//手动增加此 ArrayList 实例的容量
            trimToSize()		//将此 ArrayList 实例的容量修剪为列表的当前大小
            
            CopyOnWriteArrayList		//使用 AQS 实现线程安全
		LinkedList:链表格式
		Vector:数组格式，线程安全

	Set		//根据哈希值排序
    	TreeSet:表格式，可以排序
		HashSet:表格式
			LinkedHashSet //根据插入顺序设置链表的表
			
	Queue
        Deque		//双向队列
            ArrayDeque:使用可调整大小的数组实现
                addFirst()		//往首端插入元素
                addLast()		//往尾端插入元素
                doubleCapacity()		//使数组容量翻倍
                pollFirst()		//弹出首端数据
                pollLast()		//弹出尾端数据
                peekFirst()		//查看首端数据
                peekLast()		//查看尾端数据

        AbstractQueue		//队列操作
            poll():获取并删除队首元素
            peek():获取队首元素
            offer( E ):插入元素

            ConcurrentLinkedQueue:CAS队列
            PriorityQueue:小顶堆
            
        BlockingQueue		//阻塞队列
        	ArrayBlockingQueue:由数组支持的有界阻塞队列
```

```java
Collection 常用方法:
	add()		//添加单个元素
	addAll()		//将其他集合赋给指定集合
	remove()		//删除指定下标或元素并将元素返回
	removeAll()		//删除与其他集合重合的内容
	contains()		//查找指定元素是否存在
	size()		//返回元素个数
	isEmpty()		//判断是否为空
	clear()		//清空元素
	indexOf()		//返回指定元素在集合中首次出现的位置
	lasetIndexOf()		//返回指定元素在集合中末次出现的位置
	set(1,"")		//替换指定下标元素
	subList(1,1)		//返回指定范围的元素
    iterator()		//返回迭代器对象
```

```JAVA
Iterator 常用方法:
	hasNext()		//判断是否还有下一个对象
	next()		//返回下一个对象
    remove()		//删除下一个对象
    iterator()		//返回集合的迭代器
    forEach( Consumer )		//对Iterable的每个元素执行给定的操作
```

```JAVA
Map 常用方法:	
	put(key,vla)	//添加
	remove()		//删除指定 key
	get()		//获取指定 key 的值
	size()		//获取元素个数
	isEmpty()		//判断个数是否为0
	clear()		//清除元素
	containsKey()	//查找指定 key 是否存在
	keySet()		//返回所有的 key
	entrySet()	//返回所有关系
	values()		//返回所有值
```



1. Map中还有Map.Entry,表示一对键值对



### IO流

File	文件类

Reader		字符输入流抽象基类

Writer		字符输出流抽象基类

InputStream		字节输入流抽象基类

OutputStream		字节输出流抽象基类

Buffer		特定基元类型数据的容器

Files		此类仅包含对文件、目录或其他类型的文件进行操作的静态方法



```
Serializable		类的可序列化性标准
    其实现类:
        URL		//统一资源定位器
            openStream():打开到此URL的连接，并返回一个InputStream以从该连接读取
        InetAddress		//表示 Internet 协议（IP）地址
```

```
字节流:
    InputStream 实现类:
        FileInputStream //文件输入流
        BufferedInputStream //缓冲流
        ObjectInputStream	//对象输入流
    OutputStream 实现类:
        FileOutputStream //文件输出流
        BufferedOutpuStream //缓冲流
        ObjectOutputStream	//对象输出流
        PrintStream	//打印流
```

```
字符流:
    Writer 实现类:
        FileWriter		//文件输出流
        BufferedWriter		//缓冲流
        OutputStreamWriter		//转换流
        PrintWriter		//打印流

    Reader 实现类:
        FileReader		//文件输入流
        BufferedReader		//缓冲流
        InputStreamReader		//转换流
```

```java
File 常用方法:
    createNewFile()	//根据传入路径创建文件
    getName()	//返回文件名字
    getAbsolutePath()	//返回文件绝对路径
    getParent()	//返回文件父级目录
    length()	//文件大小
    exists()	//文件是否存在
    isFile()	//是否为文件
    isDirectory()	//是否为目录
    delete()	//删除空目录或文件,成功返回true
    mkdir()		//创建一级目录,成功返回true
    mkdirs()	//创建多级目录,成功返回true
```

```java
对象输入/输出流常用方法:
    write...()	//将对象序列化至文件,write后填数据类型,字符串是UTF,其他类是Object
    read...()	//将文件中的序列化数据读取为对象,fead 后填数据类型
```

```java
输入流常用方法:
    read()		//读取下一个字节，如果没有则返回-1
    read( byte[] )		//将读取到的数据放在 byte 数组中，该方法实际上调用read(byte[] int int)方法
    read( byte[] int int )		//从第一个 int 数据指定位置开始读取数据到 byte[] 中,到第二个 int 数据指定位置结束
	skip( long )		//跳过指定个数的字节不读取
    available()		//返回可读的字节数量
    close()		//读取完，关闭流，释放资源
    flush()		//清除文件传输缓存
    readLine()		//读取一行字符串,结束返回空，字符流的缓冲流
    available()		//获取文件的字节数
        
    mark( int )		//标记读取位置，下次还可以从这里开始读取
    reset()		//重置读取位置为上次 mark 标记的位置
    markSupported()		//判断当前流是否支持标记流，和上面两个方法配套使用
```

```java
输出流常用方法:
    write()	//将字节输入文件,没有文件会创建文件再输入
    newLine()	//输出一个换行符，字符流的缓冲流
    close()	//关闭文件链接
    flush()	//清除文件传输缓存
```

```
Buffer 实现类:
	MappedByteBuffer		//一种直接字节缓冲区，其内容是文件的内存映射区域
		force()		//强制将对此缓冲区内容所做的任何更改写入包含映射文件的存储设备
```

```
Files 方法:
	find( Path int BiPredicate FileVisitOption... )		//通过在以给定起始文件为根的文件树中搜索文件,返回一个用Path惰性填充的流
	walk( Path int FileVisitOption... )		//通过遍历以给定起始文件为根的文件树,同上
	readAllLines( Path Charset )		//读取文件中的所有行
	lines( Path Charset )		//将文件中的所有行作为流读取
	newBufferedReader( Path Charset )		//返回一个BufferedReader
		...( Path Charset ):使用指定的字符集将文件中的字节解码为字符
	newBufferedWriter( Path Charset OpenOption... )		//返回一个BufferedWriter
```



1. File 创建的时候需要传入路径，有两个行参，合起来为路径就行
2. IO 流创建的时候需要将链接的文件的路径传入,也可以传入 File 对象
3. 输出流创建时可以设定输出模式,true为增加,默认为覆盖
4. 只有实现了 Serializable 或 Externalizable 接口的类才支持序列化
5. 被 static  或 transient 关键字修饰的属性将不被序列化
6. 转换流可以将字节流转换为字符流并设置编码格式,格式为: (字节流,"编码格式")
7. 打印流可以接收 System.out 流并使用其中的方法



#### Reactor

AbstractInterruptibleChannel		可中断通道的基本实现类

InetSocketAddress		实现了SocketAddress,表示一个IP套接字地址: IP地址+端口号

AsynchronousChannel		支持异步IO操作的通道



```
AbstractInterruptibleChannel 实现类:
	SelectableChannel		//可通过选择器多路复用的通道
		register( Selector int ):向给定选择器注册此通道，并返回选择键
```

```
AsynchronousChannel 实现类:
	AsynchronousServerSocketChannel		//面向流侦听套接字的异步通道
	AsynchronousSocketChannel		//...连接套接字的异步通道
```

```
SelectableChannel 子类:
    AbstractSelectableChannel		//可选通道的基本实现类
    	子类:
            ServerSocketChannel		//应用服务器程序的监听通道
                accept():接受与此频道套接字的连接
                bind( SocketAddress ):绑定套接字的本地地址
            DatagramChannel		//UDP 数据报文的监听通道
```

```
AbstractInterruptibleChannel 方法:
	configureBlocking( boolean ):设置通道阻塞模式,只有设置成 false 才可注册选择器
	close():关闭此通道
```

```
Selector		SelectableChannel 对象的多路复用器
    select():用于等待客户端的连接到达
	open():创建选择器
	selectedKeys():返回此选择器的选定键集
	
SelectionKey		表示 SelectableChannel 向 Selector 注册的令牌
	方法:
        attach( Object )		//设置此 Reactor 的 Acceptor
        attachment()		//检索当前 Acceptor
        interestOps( int )		//将此键的集设置为给定值
        isReadable()		//是否支持读取操作
        isWritable()		//是否支持写操作
	属性:
        OP_ACCEPT		//已准备好接受另一个连接，或者有一个挂起的错误
        OP_READ		//读取操作
        OP_WRITE		//写入操作
```

```
InetSocketAddress 方法:
	InetSocketAddress( int )		//创建套接字地址,其中IP地址为通配符地址,端口号为指定值
```



1.  Reactor 模型总共有三层,分别是 Reactor,Acceptor和Handler
2.  ServerSocketChannel 通道只能注册 SelectionKey.OP_ACCEPT 事件



### 多线程

Thread 		多线程实现类

Runnable 		多线程接口

Lock		更广泛的锁操作

ThreadLocal<T>		提供线程局部变量



```
Executors		//获取线程资源的工厂类
	方法:
        newCachedThreadPool()		//返回 ExecutorService 对象
        newWorkStealingPool()		//返回拥有JVM可用处理数并行级别的 ExecutorService
             ExecutorService
               execute(Thread)    //将线程放入池中进行执行
            ...( int ):指定并行级别
        newFixedThreadPool( int )		//返回运行固定数量线程的线程池
        newSingleThreadExecutor();     //单任务线程池
        newCachedThreadPool()         //可变尺寸的线程池 可根据需要创建新线程的线程池，但是在以前构造的线程可用时将重用它们。    newScheduledThreadPool()      //延迟连接池
        /**
        它可以在给定的延迟时间后执行命令，或者定期执行命令，它比Timer更强大更灵活。ScheduledThreadPoolExecutor具有固定线程个数，适用于需要多个后台线程执行周期任务，并且为了满足资源管理需求而限制后台线程数量的场景它适用于单个后台线程执行周期任务，并且保证顺序一致执行的场景。
        */ 
        // 使用延迟执行风格的方法
           pool.schedule(t2,1000, TimeUnit.MILLISECONDS);
       // 将线程放入池中进行执行
           pool.execute(t1);    

ExecutorService		//处理线程并生成线程的 Future 对象
	方法:
        newFixedThreadPool( int ):创建一个在共享无边界队列中运行的固定数量的线程线程池
        shutdownNow():停止所有正在执行的线程,停止处理等待的任务,并返回等待执行的线程列表
        submit( Runnable ):返回该线程的 Future 对象
```

```
Lock 方法:
	lock()		//获取锁
	unlock()		//释放锁
	tryLock()		//尝试获取锁,返回结果
		tryLock( long TimeUtil ):设置等待时间
			long		//量
			TimeUtil		//单位
	newCondition()		//返回绑定此 Lock 实例的 Condition 实例
		Condition:实现线程之间的协调
			signalAll()		//唤醒所有等待的线程
			signal()		//唤醒一个等待的线程
			await()		//使当前线程等待
```

```
关键字：
	synchronized 		//线程同步修饰符
	volatile		//值同步修饰符,设置了此修饰符后对值的修改会立刻保存进内存
```

```java
Thread 方法:
	setName()	//设置线程名称
    getName()	//返回线程名称
    start()		//执行线程
    setPriority()	//更改线程优先级
    getPriority()	//获取线程优先级
    interrupt()		//中断线程的休眠
    join()		//使当前线程等待此线程执行完毕再执行
    setDaemon()		//是否设为守护线程
        
Thread 静态方法:
	currentThread()		//返回当前正在执行的线程
    sleep( long )			//让当前线程休眠，单位为毫秒
    yield()			//根据资源情况决定是否让此线程先执行
```

```
Object 线程方法:
	wait()		//使当前线程等待,直到另一个线程为此线程调用 notify() 方法或 notifyAll() 方法
	notifyAll()		//唤醒在此对象监视器上等待的所有线程
	notify()		//唤醒正在该对象监视器上等待的单个线程
```

```
ThreadLocal 方法:
	initialValue()		//设置资源的生成,需要重写实现
	get()		//返回此线程本地变量的当前线程副本中的值
	set( T )		//修改此线程对应的值
```



1. 继承 Thread 类，或实现 Runnable 接口，重写 run 方法设置线程执行的代码
2. 使用 start 方法才能创建线程, run 方法只是设置执行的代码
3. Runnable 想使用 start 方法需要将对象赋给 Thread 对象，用 Thread 对象执行
4. 每个线程都有自己独立的缓冲区,基于 JMM 来将数据同步进主存
5. 如果一个线程操作的数据与另一个线程有关,那么称这俩个线程之间存在 happens-before 关系
6. JMM 在编译后会重新给代码排序,可能会导致不同线程之间的读写 bug ,使用了 synchronized 修饰符会保证执行的顺序一致
7. 锁的状态初始为0,在锁中调用的方法如果是同一个对象或class,会自动获取锁,并有 Monitorenter 和 Monitorexit 指令
8. 守护线程要定义在执行之前



#### JUC



##### AQS

AbstractQueuedSynchronizer		构建锁和同步器的框架



```
AbstractQueuedSynchronizer 的模板方法:
	isHeldExclusively()		//该线程是否正在独占资源,只有用到condition才需要实现
	tryAcquire( int )		//独占方式,尝试获取资源
	tryRelease( int )		//独占方式,尝试释放资源
	tryAcquireShared( int )		//共享方式,尝试获取资源 
	tryReleaseShared( int )		//共享方式,尝试释放资源
```

```
AbstractQueuedSynchronizer 内部类:
	Node		//被阻塞的线程
		CANCELLED:表示当前的线程被取消
		SIGNAL:表示当前节点的后继节点包含的线程需要运行,需要进行unpark操作
		CONDITION:表示当前节点在等待condition,也就是在condition queue中
		PROPAGATE:表示当前场景下后续的acquireShared能够得以执行
		
	ConditionObject		//存放阻塞线程的CLH队列
		属性:
            firstWaiter		//头结点
            lastWaiter		//尾结点
		方法:
			addConditionWaiter()		//向队列添加 Node
			signal()		//唤醒一个等待线程
			signalAll()		//唤醒所有等待线程
			awaitUninterruptibly()		//使当前线程在接到信号之前一直处于等待状态
			await()		//比上面多个中断
				...( long TimeUnit ):多个达到指定时间
			awaitNanos( long )		//比上面多个指定时间
			awaitUntil( Date  )		//上面的时间改成期限
			hasWaiters()		//查询是否有正在等待此条件的任何线程
			getWaitQueueLength()		//返回正在等待此条件的线程数估计值
			getWaitingThreads()		//返回包含那些可能正在等待此条件的线程集合
```

```
AQS 的方法:
	acquire( int )		//以独占模式获取对象,忽略中断
	release( int )		//以独占模式释放对象
```



1. AQS 使用 CLH队列锁 实现将暂时获取不到锁的线程加入到队列中
2. tryAcquireShared 模板方法返回负数表示失败;0表示成功,但没有剩余可用资源;正数表示成功,且有剩余资源



###### CAS

AtomicInteger		基于CAS进行更新数据

Unsafe		提供一些用于执行低级别、不安全操作的方法



```
AtomicInteger 方法:
    get()		//获取当前的值
    getAndSet( int )		//获取当前的值，并设置新的值
    getAndIncrement()		//获取当前的值，并自增
    getAndDecrement()		//获取当前的值，并自减
    getAndAdd( int )		//获取当前的值，并与参数相加
    lazySet( int )		//设置为给定值,使用 unsafe.putOrderedInt 方法实现
```

```
Unsafe 方法:
	内存操作:
        allocateMemory( long )		//分配内存, 相当于C++的malloc函数
        reallocateMemory( long long )		//扩充内存
        freeMemory( long )		//释放内存
        setMemory( Object long long long )		//在给定的内存块中设置值
        copyMemory( Object long Object long long )		//内存拷贝
        getObject( Object long )		//获取给定地址值,忽略修饰限定符的访问限制
        putObject( Object long Object)		//为给定地址设置值,同上
        getByte( long )		//获取给定地址的byte类型的值
        putByte( long byte )		//为给定地址设置byte类型的值
	线程调度:
        unpark( Object )		//取消阻塞线程
        park( boolean long )		//阻塞线程
        monitorEnter( Object )		//获得对象锁(可重入锁)
        monitorExit( Object )		//释放对象锁
        tryMonitorEnter( Object )		//尝试获取对象锁
    Class 相关:
    	staticFieldOffset( Field )		//获取给定静态字段的内存地址偏移量
    	staticFieldBase( Field )		//获取一个静态类中给定字段的对象指针
    	shouldBeInitialized( Class<?> )		//判断是否需要初始化一个类
    	ensureClassInitialized( Class<?> )		//检测给定的类是否已经初始化
    	defineClass(...)		//定义一个类，此方法会跳过JVM的所有安全检查
    	defineAnonymousClass(...)		//定义一个匿名类
    对象操作:
    	objectFieldOffset( Field )		//返回对象成员属性在内存地址相对于此对象的内存地址的偏移量
    	getObject( Object long )		//获得给定对象的指定地址偏移量的值
    	putObject( Object long Object )		//给定对象的指定地址偏移量设值
    	getObjectVolatile( Object long )		//从对象的指定偏移量处获取变量的引用
    	putObjectVolatile( Object long Object )		//存储变量的引用到对象的指定的偏移量处
    	putOrderedObject( Object long long )		//有序、延迟版本的putObjectVolatile方法
    	allocateInstance( Class<?> )		//绕过构造方法,初始化代码来创建对象
    数组相关:
    	arrayBaseOffset( Class<?> )		//返回数组中第一个元素的偏移地址
    	arrayIndexScale( Class<?> )		//返回数组中一个元素占用的大小
    内存屏障:
    	loadFence()		//禁止load操作重排序
    	storeFence()		//禁止store操作重排序
    	fullFence()		//禁止load,store操作重排序
    系统相关:
    	addressSize()		//返回系统指针的大小
    	pageSize()		//内存页的大小,此值为2的幂次方
```

```
原子类:
	基本类型:
		AtomicBoolean		//原子更新布尔类型
        AtomicInteger		//原子更新整型
        AtomicLong		//原子更新长整型
    数组:
    	AtomicIntegerArray		//原子更新整型数组里的元素
    	AtomicLongArray		//原子更新长整型数组里的元素
    	AtomicReferenceArray		//原子更新引用类型数组里的元素
   	引用类型:
   		AtomicReference		//原子更新引用类型
   		AtomicStampedReference		//原子更新引用类型
   		AtomicMarkableReferce		//原子更新带有标记位的引用类型
   	字段类:
   		AtomicIntegerFieldUpdater		//原子更新整型的字段的更新器
   		AtomicLongFieldUpdater		//原子更新长整型字段的更新器
   		AtomicReferenceFieldUpdater		//原子更新引用字段的更新器
```



1. CAS是靠硬件实现的，JVM只是封装了汇编调用
2. Java原子类是通过UnSafe类实现的
3. Unsafe 实例可通过反射获取



###### park

LockSupport		用于创建锁和其他同步类的基本线程阻塞原语



```
LockSupport 的属性:
	UNSAFE		//Unsafe 实例
	表示内存偏移地址:
        parkBlockerOffset
        SEED
        PROBE
        SECONDARY

LockSupport 的方法:
	parkNanos( long )		//禁用当前线程,直到指定的等待时间
	parkUntil( Object long )		//禁用当前线程，直到指定的截止日期
	unpark( Thread )		//使给定线程的许可证可用
	getBlocker( Thread )		//返回最近一次调用 park 的线程的引用
	park( Object )		//除非许可证可用,否则禁用当前线程
```



1. LockSupport的核心函数都是基于Unsafe类中定义的park和unpark函数



###### AQS 用例

ReentrantLock		可重入互斥锁

ReentrantReadWriteLock		使用 ReadWriteLock 实现,有与 ReentrantLock 有相似的结构

ConcurrentHashMap		采用分段锁机制的 HashMap

StampedLock		具有三种模式的基于能力的锁



```
StampedLock 方法:
	writeLock()		//独占获取锁,必要时阻塞直到可用
	unlockRead( long )		//如果锁定状态与给定的标记匹配,则释放独占锁定
	tryOptimisticRead()		//返回一个稍后可以验证的标记,如果以独占方式锁定,则返回零
	validate( long )		//如果标记为0返回false
	readLock()		//以非独占方式获取锁,必要时阻塞直到可用
	tryConvertToWriteLock( long )		//将读锁转换为写锁
	unlock( long )		//如果锁定状态与给定的标记匹配,则释放相应的锁定模式
```

```
ReentrantLock 内部类
	Sync		//此锁的同步控制基础,使用AQS状态表示锁的保持数
		readObject( ObjectInputStream )		//自定义反序列化逻辑
		nonfairTryAcquire( int )		//非公平方式获取锁
		tryRelease( int )		//试图在共享模式下获取对象状态
		isHeldExclusively()		//判断资源是否被当前线程占有
		getOwner()		//返回资源的占用线程
		isLocked()		//资源是否被占用
		
	NonfairSync		//继承Sync,采用非公平策略获取锁
	FairSyn		//继承Sync,采用公平策略获取锁
```

```
ReentrantReadWriteLock 内部类
	Sync...		//基本同上
		属性:
			SHARED_SHIFT		//锁状态,高16是读,低16位是写
			SHARED_UNIT		//读锁单位
			MAX_COUNT		//读锁最大数量
			EXCLUSIVE_MASK		//写锁最大数量
		方法:
			sharedCount( int )		//占有读锁的线程数量
			exclusiveCount( int )		//占有写锁的线程数量
			tryRelease( int )		//释放写锁资源
			tryAcquire( int )		//获取写锁
			tryReleaseShared( int )		//读锁线程释放锁
			tryAcquireShared( int )		//读锁线程获取读锁
	ThreadLocalHoldCounter		//ThreadLocal子类,为了反序列化机制
```

```
ConcurrentHashMap 内部类:
	Segment		//代表一段数据,继承了 ReentrantLock 来加锁
```



1. ReentrantLock 根据 Sync 的实现类是 NonfairSync 还是 FairSyn 决定锁类型
2. synchronized是在JVM层面上实现的,在代码执行时出现异常，JVM会自动释放锁定
3. StampedLock的状态由版本和模式组成,锁获取方法返回表示和控制关于锁状态的访问的标记



##### 线程池

ThreadPoolExecutor		线程池



```
ThreadPoolExecutor 继承类:
	ScheduledThreadPoolExecutor		//提供延迟或周期执行,固定核心线程数大小
		属性:
			continueExistingPeriodicTasksAfterShutdown		//关闭后是否执行已经存在的周期任务
			executeExistingDelayedTasksAfterShutdown 		//...延时任务
			removeOnCancel 		//任务取消后是否从队列中移除
			sequencer		//相同延时的任务的顺序编号,用于保证顺序
		构造函数:
			ScheduledThreadPoolExecutor( int ThreadFactory RejectedExecutionHandler )
				int:池中要保留的线程数
				ThreadFactory:执行器创建新线程时要使用的工厂
				RejectedExecutionHandler:当由于达到线程边界和队列容量而阻止执行时要使用的处理程序
		方法:
			schedule( Callable long TimeUnit )		//用于执行一次性(延迟)任务
			scheduleAtFixedRate(...)		//创建一个周期执行的任务,不等待执行完成就开始计时				scheduleWithFixedDelay(...)		//...执行完延迟指定时间后开始下一次执行
			onShutdown()		//取消并清除由于关闭策略不应该运行的所有任务
```

```
ThreadPoolExecutor 的方法:
	execute( Runnable )		//将来某个时候执行给定任务,该任务可以在新线程或现有池线程中执行
	addWorker( Runnable boolean )		//检查是否可以添加新工作线程
	getTask()		//从阻塞队列中获取等待的任务
	shutdown()		//启动有序关闭,执行先前提交的任务,但不接受新任务
	shutdownNow()		//尝试停止所有正在执行的任务
	
ThreadPoolExecutor 内部类:
	Worker		//维护运行任务的线程的中断控制状态
        runWorker( Worker ):重复从队列中获取任务并执行它们
```

```
ScheduledThreadPoolExecutor 内部类:
	ScheduledFutureTask		//继承了FutureTask的可延迟计算
		属性:
			sequenceNumber		//为相同延时任务提供的顺序编号
			time		//任务可以执行的时间
			period		//重复任务的执行周期时间
			outerTask		//重新入队的任务
			heapIndex		//延迟队列的索引
		方法:
            setNextRunTime():设置下一次执行任务的时间
            reExecutePeriodic( RunnableScheduledFuture<?> ):重排序一个周期任务
            run()		//重写了 FutureTask 的 run 方法,实现执行周期任务时重置/重排序任务
	DelayedWorkQueue		//专用延迟队列
```



###### 任务

Future		一个任务的生命周期

Callable		返回结果并可能引发异常的任务,泛型为计算返回的数据类型



```
Future 实现类:
	FutureTask		//一种可取消的异步计算
```

```
FutureTask 的方法:
	cancel( boolean )		//取消异步任务的执行,参数决定是否中断任务
    isCancelled()		//任务是否被取消
    isDone()		//任务是否已经完成
    run()		//新建任务,CAS替换runner属性为当前线程
    get()		//获取任务执行结果
        ...(long timeout,Timeunit unit)		//带超时时间
FutureTask 的构造方法:
    FutureTask( Callable )		//自己创建计算对象
    FutureTask(Runnable V)		//指定可运行任务和成功完成后返回的结果

FutureTask 的属性:
	callable		//内部持有的callable任务，运行完毕后置空
	outcome		//计算结果
	runner		//运行callable的线程
	waiters		//等待线程(栈)
	state		//任务状态
		NEW:新的任务或者还没被执行完的任务
		COMPLETING:任务已经执行完成或者执行任务的时候发生异常
		NORMAL:执行结果已经保存到outcome字段
		EXCEPTIONAL:异常原因已经保存到outcome字段中
		CANCELLED:任务还没有执行完成的时候,调用了cancel(false)方法取消任务
		INTERRUPTING:任务还没有执行完成的时候,调用了cancel(true)方法取消任务
		INTERRUPTED:调用interrupt()中断任务执行线程
```



###### Fork/Join

ForkJoinTask		运行任务的抽象基类

ForkJoinWorkerThread		由执行ForkJoinTask的ForkJoinPool管理的线程

ForkJoinPool		用于运行ForkJoinTasks的ExecutorService



```
ForkJoinTask 子类:
	RecursiveTask		//实现可以递归执行
	RecursiveAction		//功能同上,无返回值
	CountedCompleter		//在任务完成执行后会触发执行一个自定义的钩子函数
	子类通用方法:
		compute()		//此任务执行的主要计算
ForkJoinTask 内部类:
	ForkJoinWorkerThreadFactory		//内部线程工厂接口,用于创建工作线程ForkJoinWorkerThread
		DefaultForkJoinWorkerThreadFactory:默认实现类
		InnocuousForkJoinWorkerThreadFactory:同上,无许可线程工厂
	EmptyTask		//内部占位类,用于替换队列中 join 的任务
	ManagedBlocker		//为 ForkJoinPool 中的任务提供扩展管理并行数的接口
	WorkQueue		//work-stealing 模式的双端任务队列,内部存放 ForkJoinTask 对象任务
		push():推送任务,仅由非共享队列中的所有者调用
		runTask( ForkJoinTask<?> )		//执行给定任务和任何剩余的本地任务
```

```
ForkJoinPool 构造器:
    ForkJoinPool(...)		//字挺多,自己追
        
ForkJoinPool 方法:
	invoke( ForkJoinTask<?> )		//执行给定任务,完成后返回其结果
	execute( ↑ )		//向池提交一个任务来异步执行,无返回结果
	submit( ↑ )		//...返回提交的任务,可通过task.get()获取执行结果
	externalPush( ↑ )		//尝试将给定任务添加到提交者当前队列
	externalSubmit( ↑ )		//externalPush 的完整版本,处理不常见的情况
	signalWork( WorkQueue[] WorkQueue )		//新建或唤醒一个工作线程
	scan( WorkQueue int )		//扫描并尝试窃取一个任务
	awaitWork( ↑ )		//等待获取任务,成功返回 true
	execLocalTasks()		//删除并执行所有本地任务
	deregisterWorker( ForkJoinWorkerThread Throwable )		//终止工作程序的最终回调
```

```
ForkJoinTask 的方法:
	fork()		//安排在当前任务正在运行的池中异步执行此任务
	join()		//完成计算后返回计算结果
	invoke()		//开始执行此任务,并等待任务完成并返回结果
	quietlyInvoke()		//不提取结果和异常
	quietlyJoin()		//同上
	doExec()		//被盗任务的主要执行方法
	isCompletedAbnormally()		//如果此任务引发异常或被取消,则返回true
	isCompletedNormally()		//如果此任务在未引发异常的情况下完成且未被取消,则返回true
```

```
ForkJoinWorkerThread 的方法:
	onStart()		//执行运行任务之前调用的钩子方法
	onTermination( Throwable )		//执行与终止此工作线程相关的清理钩子方法
```



1. Fork/Join 核心是运用分治算法执行任务,并使用工作窃取算法使线程复用
2. 当系统变量中有系统安全管理相关属性时,默认使用**InnocuousForkJoinWorkerThreadFactory**工厂创建工作线程
3. 重写 ForkJoinWorkerThread 的钩子方法必须在末尾调用此钩子方法



##### 工具类

CountDownLatch		基于AQS实现的计数器

CyclicBarrier		一种同步辅助工具,允许一组线程都等待对方到达共同的障碍点

Semaphore		计数信号灯

Phaser		一个可重复使用的同步屏障

Exchanger		一个同步点,线程可以在该点对元素进行配对和交换



```
CountDownLatch 的方法:
	countDown()		//减少锁存器的计数
	await()		//使当前线程等待,直到锁存器倒数为零
	
CountDownLatch 的内部类:
	Sync		//继承AQS
```

```
CyclicBarrier 属性:
	parties		//参与的线程数量
	barrierCommand		//最后一个进入屏障的线程执行的操作
CyclicBarrier 构造器:
	CyclicBarrier( int Runnable )		//指定parties与barrierCommand属性
CyclicBarrier 方法:
	await()		//使调用线程等待屏障
```

```
Semaphore 的内部类:
	Sync		//继承AQS,信号量的同步实现
		getPermits():获取许可
		nonfairTryAcquireShared( int ):共享模式下非公平策略获取
		tryReleaseShared( int ):共享模式下进行释放
		reducePermits( int ):根据指定的缩减量减小可用许可的数目
		drainPermits():获取并返回立即可用的所有许可
	NonfairSync		//Sync子类,表示采用非公平策略获取资源
	FairSync		//...采用公平策略获取资源
Semaphore 方法:
	acquire()		//从这个信号量获取许可,阻塞直到一个可用
		...( int )		//获取多个许可
	release()		//释放许可证,将其返回信号,线程没持有许可也会将许可总量递增一次
```

```
Phaser 属性:
	state		//主状态表示
	parent		//此相位器的父级
	root		//移相器树的根
	evenQ		//等待线程的偶数栈顶元素
	oddQ		//...奇数栈顶元素
Phaser 方法:
	register()		//注册一个新的阶段器
	bulkRegister( int )		//批量注册阶段器
	arrive()		//到达此相位器,不等待其他任务到达
	arriveAndDeregister()		//使当前线程到达相位器并撤销注册
	arriveAndAwaitAdvance()		//到达这个相位器并等待其他人
	awaitAdvance( int )		//等待该相位器的相位从给定相位值前进
	forceTermination()		//强制此移相器进入终止状态
```

```
Exchanger 内部类:
	Participant		//继承ThreadLocal,为每个线程保留唯一的一个Node节点
	Node		//保存部分交换的数据
		index:arena的下标，多个槽位的时候利用
		bound:上一次记录的Exchanger.bound
		collides:在当前bound下CAS失败的次数
		hash:用于自旋
		item:这个线程的当前项，也就是需要交换的数据
		match:做releasing操作的线程传递的项
		parked:挂起时设置线程值,其他情况下为null
Exchanger 属性:
	arena		//Node数组,消除阵列
	participant		//每线程状态
	slot		//在检测到争用之前使用的插槽
Exchanger 方法:
	exchange( V )		//等待另一个线程到达该交换点,然后将给定的对象传送给该线程,并返回该线程的对象
	slotExchange( Object boolean long )		//在启用arena之前使用交换功能
	arenaExchange( ↑ )		//启用arena时的交换功能
```



1. CountDownLatch 提供了一套阻塞调用线程和减少计数的方法,阻塞的线程将在计数归零时执行
2. CyclicBarrier 会在调用了 await 方法的线程还不等于 parties 时将所有调用线程阻塞,可复用
3. Semaphore 定义了一套资源分发机制,获取许可的线程将在许可不足时被阻塞,直到许可足够
4. 单独使用Semaphore不会使用到AQS的条件队列,只有进行await操作才会进入条件队列,其他的都是在同步队列中



### 网络

InetAddress		获取本机信息类



```java
TCP 网络协议类：
    Socket		//监控端口数据
    ServerSocket	//占用端口
```

```java
UDP 网络协议类：
    DatagramSocket	//占用端口
    DatagramPacket	//传输或接收数据
```



```java
InetAddress 常用方法:
    getLocalHost()	//获取本机 InetAddress 对象
    getByName()		//根据指定主机名或域名获取 InetAddress 对象 
    getHostAddress()	//返回 InetAddress 对象的主机名
    getHostName()		//返回 InetAddress 对象的地址
```

```java
ServerSocket 常用方法:
	accept()	//将端口的数据传给 Socket 对象
```

```java
Socket 常用方法:
    getOutputStream()	//返回输出端口地址
    getInputStream()	//返回输入端口地址
    shutdownOutput()	//设置结束标记
    newLine()		//设置结束标记
    colse()		//断开链接的端口
```

```java
DatagramSocket 常用方法:
    receive()	//将端口接收的数据传入指定 DatagramPacket 对象
    sand()	//将指定 DatagramPacket 对象发送给端口
    close()		//断开占用的端口链接
```

```java
DatagramPacket 常用方法:
    getLength()	//返回实际接收的数据数量
    getDate()	//返回接收到的数据
```



1. 想占用端口只需在创建对象时传入要占用的端口号
2. 创建 Socket 时传入地址和端口号即可链接上指定服务器的端口号
3. 使用IO流传输或接收完数据后需要执行结束标记
4. UDP 协议只能传送 DatagramPacket 对象
5. newLine() 结束标记的对面必须是用 readLine() 读取IO流
6. Socket 返回的端口地址是IO的抽象基类
7. DatagramPacket 对象在创建时需要传入一个空的 byte 数组,并给定数组的长度
8. 想用 DatagramPacket 对象传输数据需要在空的基础上加上IP地址和端口号



### 反射

Class		正在运行的 Java 应用程序中的类和接口

Method		提供有关类或接口上的单个方法的信息和对它的访问

Field		提供有关类或接口的单个字段的信息和对它们的动态访问

Constructor		提供有关类的单个构造函数的信息和访问权限

AccessibleObject		Field、Method 和 Constructor 对象的基类



```java
Class 常用方法:
	forName( String )		//返回与具有给定字符串名称的类或接口关联的 Class 对象
    getName()		//返回此 Class 对象表示的实体的名称
    getSimpleName()		//返回此类的类名
    getCanonicalName()		//返回对应类的全类名
    isInterface()		//指定的 Class 对象是否表示接口类型
    getInterfaces()		//返回此 Class 对象实现的接口数组
    newInstance()		//使用此 Class 对象的无参构造器生成对象并返回
    getFields()		//返回此 Class 对象表示的类或接口的所有可访问公共字段
    getDeclaredFields()		//返回此 Class 对象表示的类或接口声明的所有字段
    getSuperclass()		//返回表示此 Class 所表示的实体的超类的 Class
        
    getConstructors()		//返回此 Class 对象表示的类的所有公共构造函数
    getConstructor( Class<?>... )		//返回此 Class 对象表示的类的指定公共构造函数
        Class<?>... :构造器的参数列表
    getDeclaredConstructor( Class<?>... )		//返回此 Class 对象表示的类或接口的指定构造函数
    getDeclaredConstructors()		//该 Class 对象表示的类声明的所有构造函数
    
    getDeclaredField( String )		//返回一个反映此 Class 对象表示的类或接口的指定声明字段的 Field 对象
   		String:字段名
   	getDeclaredFields()		//返回此 Class 对象表示的类或接口声明的所有字段
    getField()		//返回一个反映此 Class 对象表示的类或接口的指定公共成员字段的 Field 对象
    getFields()		//返回此 Class 对象表示的类或接口的所有可访问公共字段
            
    getDeclaredMethods()		//返回此 Class 对象表示的类或接口的所有声明方法
    getDeclaredMethod( String Class<?>... )		//返回此 Class 对象表示的类或接口的指定声明方法
    getMethod( String Class<?>... )		//返回此 Class 对象表示的类或接口的指定公共成员方法
    getMethods()		//返回此 Class 对象表示的类或接口的所有公共方法
```

```java
ClassLoader 常用方法:
    newInstance( Object... )		//使用此 Constructor 对象表示的构造函数创建对象并返回
    getParameterTypes()		//返回一个 Class 对象数组,表示 Constructor 对象所表示构造方法的形参类型
    getDeclaringClass()		//返回表示该对象的 Class 对象
    getGenericParameterTypes()		//返回一个 Type 对象数组,表示 Constructor 对象所表示构造方法的形参类型
    getName()		//以字符串形式返回此构造函数的名称
    toGenericString()		//返回描述此构造函数的字符串，包括类型参数
```

```java
Method 常用方法:
    invoke( Object Object... )		//在具有指定参数的指定对象上调用此 Method 对象表示的基础方法
    	Object:从底层方法调用的对象
	    Object... :用于方法调用的参数
            
    getReturnType()		//使用 Class 对象返回此 Method 对象表示的方法的正式返回类型
    getGenericReturnType()		//使用 Type 对象返回此 Method 对象表示的方法的正式返回类型
    getParameterTypes()		//使用 Class 数组返回此对象表示的可执行文件的形式参数类型
    getGenericParameterTypes()		//使用 Type 数组返回此对象表示的可执行文件的形式参数类型
    getName()		//以 String 形式返回此 Method 对象表示的方法的名称
    isVarArgs()		//判断方法是否带可变参数
    toGenericString()		//返回描述此方法的字符串，包括类型参数
```

```java
Field 常用方法:
    get( Object )		//返回指定对象上此字段表示的字段的值
    set( Object Object )		//将指定对象参数上的此 Field 对象表示的字段设置为指定的新值
    getType()		//返回一个 Class 对象,该对象标识此 Field 对象表示的字段的声明类型
    isEnumConstant()		//此字段是否表示枚举类型的元素
    toGenericString()		//返回描述此字段的字符串,包括其通用类型
    getName()		//返回此 Field 对象表示的字段的名称
    getDeclaringClass()		//返回表示声明此 Field 对象表示的字段的类或接口的 Class 对象
```

```
AccessibleObject 方法:
	setAccessible( boolean )		//将此对象的可访问标志设置为指示的布尔值
```



1. 反射类及反射方法的获取，都是通过从列表中搜寻查找匹配的方法，所以查找性能会随类的大小方法多少而变化
2. 反射考虑了线程安全



#### 方法句柄

MethodHandle		对基础方法构造函数的类型化,可直接执行的引用

MethodHandles.Lookup		创建句柄的工厂函数

MethodType		表示方法句柄接受和返回的参数和返回类型



```
Lookup 方法:
	findGetter( Class<?> String Class<?> )		//提供对非静态字段的读取权限
		Class<?>:从中访问方法的类或接口
		String:字段的名称
		Class<?>:字段的类型
	findConstructor( Class<?> MethodType )		//使用指定类型的构造函数创建对象并初始化它
		Class<?>:从中访问方法的类或接口
		MethodType:方法的类型和void返回类型
```

```
获取 Lookup:
	MethodHandles.lookup()		//返回具有完全功能的查找对象
	MethodHandles.publicLookup()		//返回最低信任的查找对象(只能访问public)
```

```
MethodType 方法:
	methodType( Class<?> )		//设置有指定返回类型的 MethodType
        methodType( ↑ Class<?> ):再设置个参数
```

```
MethodHandle 方法:
	invoke( Object... )		//调用方法句柄
		Object... :签名多态参数列表
```



1. 方法句柄是对底层方法、构造函数、字段或类似的低级操作的类型化、可直接执行的引用，带有可选的参数或返回值转换(性能比反射和其他好)



### jdbc

Driver	驱动

DriverManager	包装驱动

Connection	数据库链接

Statement	输出sql

PreparedStatement	继承了 Statement 的加强版

ResultSet	结果集



```java
ResultSet 方法:
    next()		//向下获取一行数据,没有数据返回false
    previous()		//向上获取一行数据
    getxxx()	//提取指定数据,get后面写接收的数据的类型,下标从1开始,也可以用列名获取数据
    close()		//释放资源
```

```java
DriverManager 静态方法:
    registerDriver(Driver对象)	//建立 DriverManager 对象
    getConnection( String String String )	//尝试链接数据库,并返回链接
        String:数据库链接,格式为: "jdbc:mysql://IP地址:端口号/数据库名?serverTimezone=UTC"
        String:用户名
        String:密码
    
```

```java
Connection 常用方法:
    createStatement()		//返回一个 Statement 对象
    PreparedStatement("sql语句")		//返回一个 PreparedStatement 对象
    close()		//关闭链接
```

```java
Statement 常用方法:
    executeUpdate()		//执行增删改语句,并返回受影响的行数
    executeQuery()		//执行 selelct 语句,并返回结果集
    execute()		//执行任意sql语句,返回布尔值
    setAutoCommit()		//是否自动提交 sql,默认为 true
    commit()		//提交事务
    rollback()		//回滚事务
    addBatch()		//存储sql语句
    executeBatch()		//执行存储的sql语句
    clearBatch()		//清空存储的sql语句
    close()		//关闭链接
```

```java
PreparedStatement 方法:
	setxxx( String String)		//给占位符赋值,需指定值的类型
        String:占位符的索引
        String:值
```

```java
连接池:
    ComboPooledDataSource	//c3p0 链接实列
	DruidDataSource		//德鲁伊链接实列
```

```java
ApDBUtils 查询数据收集框架:
	DbUtils	//工具接口
		QueryRunner	//执行sql语句
		ResultSetHandler	//设置数据格式的接口
        	ScalarHandler		//将第一行第一列的数据用object类型数据返回
            ArrayHandler	//将结果集中的第一行数据转成对象数组
            ArrayListHandler	//把结果集中的每一行数据都转成一个数组,再存到list集合中
            BeanHandler		//将结果集中的第一行数据封装到一个对应的javaBean实列中
            BeanListHandler //将结果集中的每一行数据都封装到一个对应的javaBean实列中,存放到list中
            ColumnListHandler	//将结果集中某一列的数据存放到list中
            KeyedHandler(name)	//将结果集中的每行数据都封装到map中,然后放入另一个map中,指定key
            MapHander	//将结果集中的第一行数据封装到一个Map里,key是列名,value是值
            MapListHandler	//将结果集中的每一行数据都封装到一个map中,然后存到list里
```

```java
Driver 方法:
	connect("jdbc:mysql://IP地址:端口号/数据库名", Properties )	//尝试链接数据库,并返回链接
```

```java
QueryRunner 方法：
    query(参数1,参数2,参数3,...)	//执行select语句,参数1为链接对象,参数2为执行的sql语句,参数3为ResultSetHandler 的实现类对象,往后的参数为sql语句中问号填充的值
    update(参数1,参数2,....)	//执行其他sql语句,参数1为链接对象,参数2为执行的sql语句,之后的参数为?中填充的值
```

```java
ComboPooledDataSource 方法:
    setDriverClass()	//设置驱动
    setJdbcUrl()	//设置数据库对象
    setUser()	//设置用户名
    setPassword()	//设置用户密码
    setInitialPoolSize()	//设置最小连接数
    setMaxPoolSize()	//设置最大连接数
    getConnection()	//返回 Connection 对象
```

```java
DruidDataSource 方法:
    setDriverClassName()		//设置驱动的包名
    setUrl()		//设置链接字符串
    setUsername()		//设置用户名
    setPassword()		//设置密码
    setInitialSize()	//设置初始大小
    setMaxActive()		//设置最大大小
    setMinIdle()	//设置最小空闲链接
    getConnection		//返回 Connection 对象
```



1. 想向数据库输出sql语法需要先用 Connection 接收返回的链接,然后将链接赋给 statement
2. 加载 Driver 时会自动注册一个 DriverManager 对象,对象名为 DriverManager
3. 想使用批量处理sql语句需要在传入url参数时在后面加上 ?rewriteBatchedStatements=true
4. ResultSetHandler 接口实现类指定实现类对象的方法基本都是在构造器中传入实现类的class对象
5. PreparedStatement 输出的 sql 语句中可以设置 ? 来代表未定义,并于之后用方法填补
6. 使用 PreparedStatement 执行的sql语句通常在定义时就已经输入了,之后会自动调用填补后的sql语句



## JVM



### 内存



```
内存结构:
	堆:
		Young(新生代):
			Eden		//新对象
			From Survivor(幸存1区)		//还没死的
			To Survivor(幸存2区)		//同上
		Old(老年代)		//被长时间使用的对象,或大对象
		Non-Heap(元空间)		//方法区
	方法区:
		类型信息		//略
		域信息		//略
		方法信息		//略
		运行时常量池		//略
	线程栈:
		Program Counter Register(程序计数器)		//当前线程下一条指令的地址
		Native Method Stack(本地方法栈)		//调用非 Java 代码的接口
		Virtual Machine Stacks(虚拟机栈):
			Local Variables(局部变量表)		//存储方法参数和定义在方法体内的局部变量
			Operand Stack(操作数栈)		//保存计算过程的中间结果
			Dynamic Linking(动态链接)		//指向运行时常量池中该栈帧所属方法的引用
			Return Address(方法返回地址)		//存放调用该方法的 PC 寄存器的值
			附加信息		// Java 虚拟机实现相关
```



1. 如果有 this,那么将存在局部变量表的 0 下标处
2. 虚拟机栈中只有栈顶的栈帧会存在寄存器中
3. 线程栈是线程私有的,生成线程也会生成一个对应的线程栈
4. 新生代有两个幸存区主要方便使用 Copying 算法
5. 方法区用于存储已被虚拟机加载的类型信息、常量、静态变量、即时编译器编译后的代码缓存等



### 垃圾回收



```
回收分类:
	Minor GC		//只是新生代的垃圾收集
	Major GC		//只是老年代的垃圾收集
	Mixed GC		//收集整个新生代以及部分老年代的垃圾收集
	Full GC		//收集整个 Java 堆和方法区的垃圾
```

```
垃圾回收算法:
	识别:
        Reference Counting(引用计数法)		//对每个对象的引用进行计数,大于0就是存活
        Tracing GC(可达性分析)		//从 GC Root 开始搜索,标记可达对象
	
	收集:
        Mark-Sweep(标记清除)		//找完就删
        Mark-Compact(标记整理)		//存活的移动到前端,然后清空其他,
        Copying(复制)		//内存分成两块,一块活一块死
```

```
收集器:
	CMS		//Concurrent Mark Sweep,略
	G1		//引入分区,弱化分代,同时使用 Compact 和 Copying 算法,高吞吐
	ZGC		//通过着色指针和读屏障实现全并发,低延迟
```



1. Mark-Compact 步骤比 Copying 多
2. Reference Counting 算法需要使用 Recycler 算法解决循环引用问题



#### 引用

SoftReference		软引用对象

WeakReference		弱引用对象

PhantomReference		幻影引用对象



### 调优参数



```
-Xms		//堆最小值
-Xmx		//堆最大值
-Xmn		//新生代大小
-Xss		//每个线程池的堆栈大小
```

```
有 -XX: 前缀:
	NewRatio		//设置新生代与老年代比值
	PermSize		//设置持久代初始值
	MaxPermSize		//设置持久代最大值
	MaxTenuringThreshold		//新生代中对象存活次数
	SurvivorRatio		//Eden区与Subrvivor区大小的比值
	PretenureSizeThreshold		//对象超过多大值时直接在老年代中分配
	ParallelGCThreads		//指定并行的垃圾回收线程的数量
	CMSFullGCsBeforeCompaction		//在多少次GC后进行内存压缩
```



## JDK 8

### 正则表达式

Pattern		模式类，定义正则语句

Matchar		匹配器，设定被匹配的文本



```java
正则字符匹配:
    []	//匹配[]中任意的字符,不用分隔
    [^...]	//匹配不含[^...]中任意字符的
    -	//匹配什么到什么的字符,比如1-9
    .	//匹配除\n以外的字符
    \\d	//匹配单个数字字符
    \\D	//匹配单个非数字字符
    \\w	//匹配单个数字、大小写字母字符、下划线
    \\W	//匹配单个非数字、大小写字母字符、下划线
    \\s	//匹配空白字符
    \\S	//匹配非空白字符
限定符:
    ?	//前面匹配成功0次或一次,并将匹配模式改成非贪婪匹配
    +	//前面匹配成功1次或多次
    *	//前面匹配成功0次或多次
    {...}	//前面一个重复执行指定次数
	{... ,}	//前面匹配最少成功指定次数(去掉空格)
	{... , ...}	//前面匹配最少成功几次，最多成功几次(去掉空格)
定位符:
	^	//指定被匹配的字符串的起始位置
    $	//指定被匹配的字符串的结束位置
    \\b	//匹配被空格分隔的字符串的结束和整体的结束
    \\B	//匹配被空格分隔的字符串的起始和整体的起始
其他:
    |	//如果前面匹配不上则匹配后一个
    (?i)	//表示往后的字符不区分大小写
    //...	//设置内容必须为指定分组的匹配结果,从1开始,只能后调用前
捕获分组:
	(...)	//将这一部分的索引单独保存为一组,以便单独取出
    (?<...>...)	//给分组设置别名
非捕获分组:
	(?:...)	//并不会保存索引的分组,并且不会破坏原本的属性,比如"1234"和"12(?:34)"的效果是一样的
	(?=...)	//加一条判断,但并不会将判断的匹配提取,比如"12(?=34)"匹配成功后获取的是12
	(?!...)	//上面取反
```



```java
Matchar 方法:   
	find()	//保存匹配成功的索引,参数为将后置索引减少几位
    group()	//根据保存的索引从被匹配的对象中取字符,参数用于指定组
    start()	//返回本次匹配成功位置的起始下标
    end()	//返回本次匹配成功位置的结束下标
    matches()	//将正则表达式与文本进行整体匹配,并返回boolean类型
    replaceAll("参数1")	//将匹配成功的索引替换为参数1并返回替换后的字符串
```

```java
Pattern 方法：
    compile( String )	//设定正则语句并返回一个Pattern
    matcher( CharSequence )	//设置被匹配的对象并返回一个Matcher对象
        matches( String CharSequence )	//同上,从整体判断正则表达式是否匹配成功
    
Pattern 属性:
	Pattern.CASE_INSENSITIVE		//启用不区分大小写的匹配
```





1. 将正则表达式用多个()分隔时被匹配到的下标将分别存储到底层的数组中,下标0和1将存储第一个匹配的开头和最后一个匹配的结尾



### lambda 表达式

FunctionalInterface		一种信息性注释类型,用于指示接口类型声明是函数式接口



```
函数式接口:
	Consumer<T>		//无返回值方法,方法名为accept
    Supplier<T>		//有返回值方法,方法名为get
    Function<T,R>		//接收T返回R的方法,方法名为apply
    Predicote<T>		//返回布尔类型的方法
```

```
Predicote 方法:
    test( T )		//如果输入参数与表达式匹配，则为true，否则为false
```



1. lambda 表达式实际为函数式接口的实列，语法为...=(形参) -> 方法体;
2. 如果加了泛型并且泛型和形参类型一样,那么 () 之中的形参不用写类型
3. 如果只有一个形参,那么 () 可以不写
4. 当方法体有多条语句时需要用 {} 包起来
5. 当方法体只有一条语句时,如果有返回值默认那一条语句为返回值
6. lambda表达式可以用 :: 代替 . 直接调用方法
7. 在 :: 中,构造器都叫new,根据参数区分,参数会根据泛型自动匹配
8. lambda 表达式最主要作用还是将一个方法单独保存,谁都能用,和之前只能用内部类相比多了一些解决方案



### Stream

Stream		支持顺序和并行聚合操作的一系列元素

IntStream		Stream的int数据专用化



```
通过集合获取Stream对象:
    stream()		//返回顺序流
    parallelStaeam()		//返回并行流
```

```
IntStream 方法:
	range( int int )		//以递增步长1返回参数指定的范围的顺序IntStream
	summaryStatistics()		//返回一个IntSummaryStatistics
```

```
数组获取:
    Arrays.stream()		//数组流
    	数组流的返回类型:
			int[]		//返回IntStream
            long[]		//返回LongStream
            double[]		//返回DoubleStream
```

```
OF 方法获取:
    Stream.of(...)		//根据传进来的多个参数创造
```

```
创造无限流:
	limit()		//根据参数决定第几次获取数据后结束
    迭代:
		iterate("初始值","迭代方法")		//迭代生成
    生成:
		generate("方法")		//调用传入的方法,并保存返回的值
```

```java
Stream 筛选与切片方法:
	filter()		//根据传入的 Predicote 类型 lambda 表达式来决定什么数据被保存
    limit()		//根据参数决定第几次获取数据后结束
    skip()		//将前面指定数量的数据跳过
    distinct()		//根据hashCode方法和equals方法去重
```

```
Stream 映射方法:
	map( Function )		//返回由将给定函数应用于此流元素的结果组成的流
    flatMap( ↑ )		//对流的元素应用一对多转换,然后将生成的元素展平为新的流
    mapToInt( ToIntFunction )		//返回IntStream,该IntStream包含将给定函数应用于此流元素的结果
    peek( Consumer )		//返回由该流的元素组成的流,当元素被缩减将应用表达式
    reduce( T BinaryOperator<T> )		//设置初始值和应用函数,返回结果
```

```
Stream 排序方法:
	sorted( Comparator )		//返回由该流的元素组成的流,并根据提供的Comparator进行排序
		...():返回由该流的元素组成的流,并按照自然顺序排序
```

```
Stream 匹配与查找方法:
	allMatch( Predicote )		//根据表达式与Stream中所有元素匹配,并返回布尔值
    anyMatch( ↑ )		//根据表达式与Stream中至少一个元素匹配,并返回布尔值
    noneMatch( ↑ )		//根据表达式判断是否与Stream中所有元素都不匹配,并返回布尔值
    findFirst()		//返回第一个元素
    findAny()		//返回任意元素
    count()		//返回Stream中元素个数
    max()		//根据传入的lambda表达式返回最大元素
    min()		//根据传入的lambda表达式返回最小元素
```

```
Stream 收集方法:
    collect( Collector )		//使用收集器对此流的元素执行可变缩减操作
        参数可填:
            Collectors.toSet()		//将结果返回为一个set集合
            Collectors.toList()		//将结果返回为一个List集合
            Collectors.joining()		//按顺序将输入元素连接到字符串中
```



1. 集合和数组都能使用返回Stream对象的方法
2. 获取无限流的limit方法跟在实现后面,forEach方法跟在limit后面,列如:iterate(...).limit(...).forEach()
3. 顺序流使用时没有用多线程，并行流在使用时用多线程
4. Stream执行筛选后就不能再次执行筛选,但是可以同时执行多种筛选,如: filter().limit()



### Optional

Optional		一个可以为null的容器对象



```java
创建：
    of()		//创建一个Optional实列,参数必须为非空
    empty()		//创建一个空的Optional实列
    ofNullable()		//参数可以为空
```

```java
方法:
	isPresent()		//如果值存在返回true，否则返回false
    ifPresent( Consumer )		//如果Optional实例有值则为其调用consumer
    map( Function )		//返回表达式返回值的Optional
    flatMap( Function Optional )		//同上,需要包装成Optional再返回
    filter( Predicate )		//如果有值并且满足条件返回包含该值的Optional
```

```
获取:
    get()		//如果Optional有值则将其返回
    orElse( T )		//如果有值则将其返回,否则返回指定的其它值
    orElseGet( Supplier )		//同上,使用表达式生成默认值
    orElseThrow( ↑ )		//同上,否则抛出supplier接口创建的异常
```



### 时间 API

Clock		用于访问某个特定 时区的 瞬时时间、日期 和 时间

Instant			瞬时时间

ZoneId			表示时区

LocalDateTime				表示日期和时间

LocalDate					表示日期

LocalTime					表示时间

DateTimeFormatter					用于打印和解析日期时间对象的格式化程序

MonthDay					日历系统中的月日

YearMonth					日历系统中的年月

TimeUnit		给定粒度单位下的持续时间

ZonedDateTime		包含时区的完整的日期时间



```
Clock 方法:
	millis()		//返回当前瞬时时间
	
Clock 静态方法:
	systemUTC()		//系统默认UTC时钟,等效于 System.currentTimeMillis()
	systemDefaultZone()			//系统默认时区时钟
	system( ZoneId )			//指定时区的瞬时时间
	fixed( Instant ZoneId )		//返回一个不会改变的指定时区瞬时时间
	offset( Clock Duration.ofSeconds(秒数) )		//将指定 Clock 对象的瞬时时间增加指定秒数并返回
```

```
Instant 常用方法:
	getEpochSecond()		//返回一个精确到秒的瞬时时间
	toEpochMilli()			//返回一个精确到毫秒的瞬时时间
	
Instant 静态方法:
	now()	//返回一个 Instant 对象
	now( Clock )		//返回一个指定时区的瞬时时间
```

```
ZoneId 静态方法: 
	of("时区")		//返回一个指定时区的 ZoneId 对象
		Europe/Paris:巴黎时区
		Asia/Shanghai:上海时区
	systemDefault()			//返回系统默认时区
```

```
Local... 静态方法:
	now()		//使用默认时区时钟瞬时时间创建
	now( ZoneId )		//自定义时区
	now( Clock )		//从指定时钟获取时间
	ofInstant( Instant ZoneId )			//瞬时时间表示创建时间的时刻,时区表示可能的偏移量,都不为空
	parse( String )			//根据传入的字符串返回时间
	parse( String DateTimeFormatter )		//使用格式化程序解析文本，返回时间
	of()	//自定义日期时间,根据 年月日 时分秒 纳秒 的顺序来设置
	
LocalDate | LocalDateTime 的常用方法:
	getYear()		//获取年份字段
	getMonth()		//使用 Month 枚举获取月份字段
	getDayOfYear()		//获取日期字段,从 1 到 365，或闰年的 366
	getDayOfMonth()			//获取日期字段,从 1 到 31
	getDayOfWeek()		//获取星期字段
	minusDays( long )		//返回此 LocalDateTime 的副本，减去指定的天数,可以为负数
	
LocalTime | LocalDateTime 的常用方法:
	getHour()		//获取小时字段,从 0 到 23
	getMinute()			//获取分钟字段,从 0 到 59
	getSecond()			//获取秒的字段,从 0 到 59
	getNano()		//获取纳秒字段,从 0 到 999,999,999
	
Local... 的常用方法:
	plus( long TemporalUnit )			//返回此日期的副本,long - 添加到结果中的单位数量,可以是负数,另一个是数量的单位
		日期:
			IsoFields.WEEK_BASED_YEARS		//表示基于周的年的单位,单位等于 52 或 53 周
			IsoFields.QUARTER_YEARS		//代表季度概念的单位
		时间:
			ChronoUnit.NANOS		//纳秒数
			ChronoUnit.MICROS		//微秒数
			ChronoUnit.MILLIS		//毫秒数
			ChronoUnit.SECONDS		//秒数
			ChronoUnit.MINUTES		//分钟数
			ChronoUnit.HOURS		//小时数
			ChronoUnit.HALF_DAYS		//半天数
			
LocalDate 的常用方法:
	isLeapYear()		//根据 ISO 预测日历系统规则检查年份是否为闰年
```

```
DateTimeFormatter 常用方法:
	format( Local... )		//根据此格式输出时间

DateTimeFormatter 的静态方法:
	ofPattern( String )		//使用指定的模式创建格式化程序
```

```
MonthDay 的静态方法:
	of( Month int )		//Month - 要表示的月份,int - 天,从 1 到 31
	from( TemporalAccessor )		//从时态对象中获取 MonthDay 的实例
```

```
YearMonth 常用方法:
	lengthOfMonth()		//返回月份的长度

YearMonth 的静态方法:
	now()		//从默认时区的系统时钟获取当前的年月
	of( int Month )		//从年份和月份中获取 YearMonth 的实例,Month 能换成 int
```



1. LocalDateTime 中有一个 LocalDate 对象和一个 LocalTime 对象
1. MonthDay 实现了 TemporalAccessor 接口



### JavaFx

Desktop		与各种桌面功能交互



## JDK 11

ProcessHandle		标识并提供对本机进程的控制

ObjectInputFilter		反序列化期间的过滤器类,数组长度和图形度量

HttpClient		HTTP客户端

HttpRequest		HTTP请求

Flow		用于建立流控制组件的相关接口和静态方法

StackWalker		对线程的堆栈进行遍历,并且支持过滤和延迟访问



```
语言新特性:
	1. 允许在接口中使用私有方法
    2. 新增局部变量保留字 var 使变量的类型交由编译器推断
```

```
集合新增方法:
	List.of()		//创造不可变集合
	Set.of()		//同上
	Map.of()		//同上
	Map.ofEntries( Entry... )		//同上
```

```
Stream 新增方法:
	ofNullable( T )		//返回包含单个元素的连续流,如果非空,则返回空流
	dropWhile( Predicate )		//过滤与给定谓词匹配的元素
	takeWhile( Predicate )		//过滤不匹配的
	iterate( T UnaryOperator )		//返回通过将函数迭代应用于初始元素种子而产生的无限顺序流
```

```
Collectors 新增方法:
	filtering( Predicate Collector )		//根据谓词过滤元素并返回
	flatMapping( Function Collector )		//自己追
```

```
Optional 新增方法:
	ifPresentOrElse( Consumer Runnable )		//使用该值执行给定的操作
	or( Supplier )		//如果存在值,则返回描述该值的Optional,否则返回函数结果
	stream()		//如果存在值,则返回仅包含该值的连续流,否则返回空流
```

```
InputStream 新增方法:
	readAllBytes()		//从输入流中读取所有剩余字节
	readNBytes( int )		//从输入流中最多读取指定数量的字节
	transferTo(	OutputStream )		//读取此输入流中的所有字节,并按读取顺序将字节写入给定的输出流
```

```
System 新增方法:
	getLogger( String )		//返回供调用方使用的Logger实例,需指定实例名
    
System 内部类:
	Logger		//记录与 LoggerFinder 的消息映射
```

```
CompletableFuture 新增方法:
	completeAsync( Supplier )		//使用默认的执行器从异步任务调用给定函数完成任务
		...( ↑ Executor )		//指定执行器
	orTimeout( long TimeUnit )		//设置有限定时间的任务
	completeOnTimeout( T long TimeUnit )		//如果超时则返回指定值
```

```
Thread 新增方法:
	onSpinWait()		//表示调用方暂时无法继续
```



```
Logger 方法:
	log( Level String )		//记录消息
```

```
HttpRequest 方法:
	uri( URI )		//设置此HttpRequest的请求URI
	build()		//生成并返回HttpRequest
```

```
HttpClient 方法:
	sendAsync( HttpRequest BodyHandler )		//异步发送给定请求
```



1. ProcessHandle 实例可通过 Process.toHandle() 方法获取
1. JVM 在运行时只有一个系统范围的 LoggerFinder 实例
1. MessageDigest 新增4 个 SHA-3 哈希算法: SHA3-224、SHA3-256、SHA3-384 和 SHA3-512
1. 新增 ZGC 垃圾回收器



### 变量句柄

VarHandle		变量的动态强类型引用



```
Lookup 变量句柄方法:
	findVarHandle( Class<?> String Class<?> )		//访问非静态字段名
		Class<?>:字段所属对象
		String:字段名
		Class<?>:字段类型
	findStaticVarHandle( ↑ )		//访问静态字段名
```

```
VarHandle 方法:
	get( Object... )		//普通读取访问
	getVolatile( ↑ )		//volatile 读取访问
	getOpaque( ↑ )		//按程序顺序访问
	getAcquire		//确保在此访问之前不会对后续加载和存储进行重新排序
```

```
新增方法句柄工厂函数: 
	arrayConstructor( Class<?> )		//生成一个方法句柄来构造所需类型的数组
	arrayLength( ↑ )		//生成返回数组长度的方法句柄
	varHandleInvoker( VarHandle.AccessMode MethodType )		//调用 VarHandle 中的访问模式方法
	varHandleExactInvoker( ↑ )		//同上
	zero( Class<?> )		//生成请求的返回类型的常量方法句柄
	loop( MethodHandle[]... )		//表示一个具有多个循环变量的循环
	countedLoop( MethodHandle MethodHandle MethodHandle )		//循环运行给定次数的迭代
	iteratedLoop( ↑ )		//Iterator＜T＞
	whileLoop( ↑ )		//构造while循环
	doWhileLoop( ↑ )		//构造do while循环
	tryFinally( MethodHandle MethodHandle )		//将目标方法句柄包装在try finally块中
```



## JDK 17

RecordComponent		提供有关Records类的组件的信息和对该组件的动态访问

Proxy		可以定义隐藏类作为实现代理接口的代理类

StringConcatFactory 		可以生成隐藏类来保存常量连接方法

LambdaMetaFactory 		可以生成隐藏的nestmate类,以容纳访问封闭变量的lambda主体

MemorySegment 		内存段模拟内存的连续区域



```
switch 表达式:
    switch (i) {
        case 1, 2, 3 -> 6;
        default -> 0;
    }
	
1. -> 符号右则表达式方法体在执行完分支方法之后,自动结束 switch 分支
2. -> 右则方法块中可以是表达式、代码块或者是手动抛出的异常
3. 现在直接使用 yield 关键字来返回 case 分支需要返回的结果
```

```
文本块:
	String query = """
    	SELECT * from USER 
        WHERE `id` = 1 
        ORDER BY `id`, `name`;
    """;
    
    文本块转义符:
    	\		//行终止符
    	\s		//表示一个空格
    
1. 使用3对 "" 符号来定义文本块
2. 可以避免使用大多数转义符号，自动以可预测的方式格式化字符串
```

```
instanceof 模式匹配:
	匹配变量 instanceof 类名 i
	
1. 如果类型匹配成功,则会转换为指定类型,并赋值给模式局部变量 i
```

```
Records类型:
	public record Person(String name, int age){
		...
	}
	
1. Record 类型允许在代码中使用紧凑的语法形式来声明类
2. 当用 Record 来声明一个类时,该类将自动拥有下面特征:
	1.拥有一个构造方法获取和成员属性值的方法：name()、age()
	2.hashCode() 方法和 euqals() 方法
	3.toString() 方法
	4.类对象和属性被 final 关键字修饰，不能被继承，类的示例属性也都被 final 修饰，不能再被赋值使用
	5.还可以在 Record 声明的类中定义静态属性、方法和示例方法
```

```
密封的类和接口:
	sealed class | interfaces permits ... {
		...
	}
	
1. 这些class或者interfaces只允许被指定的类或者interface进行扩展和实现
2. 关键字permits列出可以直接扩展它的类,子类可以是 final 的,non-sealed 的或 sealed 的
```



```
Socket 重构:
    NioSocketImpl		//基于NIO的SocketImpl
```

```
Class 新增方法:
	isRecord()		//仅当此类是 Record 类时,返回true
	getRecordComponents()		//返回表示该Record类的所有Record组件的RecordComponent对象数组
```

```
DatagramSocket 重构:
	//没看
```

```
@Deprecated 增强:
	since()		//返回批注元素已弃用的版本
	forRemoval()		//指示是否在将来的版本中删除带注释的元素,默认值为false
```

```
新增注解:
	ValueBased		//指示所讨论的API声明与基于值的类相关联
```

```
增强的伪随机数生成器:
	RandomGenerator		//为生成随机或伪随机数字序列的对象提供通用协议
		方法:
			of( String )		//返回使用指定名称算法的RandomGenerator实例
```

```
String 新增方法:
	stripIndent()		//从文本块中去除空白字符
	translateEscapes()		//翻译转义字符
	formatted( Object... )		//格式化
```



1. 删除 CMS 垃圾收集器



### Vector 

VectorSpecies		用于管理元素类型和形状的相同组合的所有矢量的接口

FloatVector		表示浮点值的有序不可变序列
