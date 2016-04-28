# 预处理

#####  c语言处理过程：.c文件-->(预处理).i文件---->(编译).s文件--->(汇编).o文件
* gcc -o  helloworld.i   helloworld.c  -E   将helloworld.c文件预处理成helloworld.i文件,-E表示只让gcc做预处理；
* gcc -S  helloworld.i  -o helloworld.s       将helloworld.i文件编译成helloworld.s文件,-S表示只让gcc做编译；
* gcc -C  helloworld.s  -o helloworld.o    	  将helloworld.s文件汇编成helloworld.o文件,-C表示只让gcc做汇编；

##### 宏替换（发生在预处理阶段的单纯的字符串替换,好处是可以不考虑数据类型）   
* 宏常量
```c
#define MAX 3
```

* 宏函数    
```c
#define N(n) n*10   //带一个参数的宏函数
int b=N(a);//在编译阶段将会被替换成:int b=a*10;
#define ADD(a,b) (a+b)  //带两个参数的宏函数   
``` 

##### typedef
```c
typedef int* p;//使用p代替类型int*,就是给int*起一个别名
```

