### 数据类型
1. char
2. short
3. int
4. long
5. long long
6. float
7. double
8. 字符类型的本质是1个字节的整型 比如a=97
### printf函数
1. %c，%d，%f，%lf，%p
### sizeof函数，变量/类型所占空间大小
1. sizeof(char)
2. sizeof(int)
### 取地址符号 &，scanf函数
1. &num
### 变量，
### 常量
1. 字面常量
2. const
3. define 定义标识符常量
4. 枚举常量
### 字符串
1. char arr[] = "abc"
2. char arr1[] = {'a', 'b', 'c', '\0'} 或  {'a', 'b', 'c', 0} 因为字符 '\0' 的值即为 0
3. '\0' 为字符串结束标志，不算字符串内容，不被计算为字符串长度
4. strlen计算字符串长度，不以'\0'结尾的字符串返回随机值，因为它会去查找后续内存空间直到遇到'\0'

### 关键字
1. typedef 类型定义/类型重定义

typedef unsigned int u_int 
unsigned int num = 20;

1. static 修饰局部变量，局部变量的生命周期变长
2. static 修饰全局变量，让全局变量只能在全局变量所在的源文件内部使用
3. static 修饰函数，是其外部链接属性变为内部链接属性，不能被外部文件引用

### #define 定义常量
1. #defind MAX 100
### #define 定义宏 - 带参数，定义一段替换的代码
1. #define MAX(X, Y) (X>Y?X:Y)


### 数组
1. 一组同类型元素的集合
2. int arr[10];
3. arr[下标]
4. 数组名+1和数组地址+1问题，指针类型不一样
5. 数组名是数组首元素地址
### 操作符
### 关键字






### 选择，循环
1. if/else,switch,while,do...while,for
2. else 和离得最近的 if 进行匹配

### 函数
1. 函数声明，函数定义，函数调用
2. 递归


### 操作符
1. 移位操作符
2. 位操作符
3. sizeof 中的表达式是不会计算的
4. 按位取反 ～
5. 强制类型转换
6. char类型的整型提升

### 指针
1. 一个内存单元为1个字节
2. 指针类型，存放地址的变量类型
int a = 10;
int* p = &a;
3. 解引用操作符，间接访问操作符
*p = 20; 通过指针p找到变量a，将a的值改为了20
4. char类型的指针类型
char c = 'a';
char* p = &c;

5. 指针类型的意义
- 指针类型决定了指针进行解引用操作时能够访问空间的大小
- 指针加减整数时，指针偏移空间的大小。比如int* 偏移4个字节，char* 偏移1个字节

6. 野指针
- 非法访问内存


### 结构体
```c
// 定义
struct Book {
  char name[20];
  short price;
};

// 创建
struct Book b1 = {"ABC", 88};

// 访问成员
b1.name;
b1.price;

// 指针类型
struct Book* p = &b1;
// 利用指针访问成员
(*p).name;
(*p).price;
p->name;
p->price;

```