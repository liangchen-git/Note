# 段

> 可执行程序的组成部分

### 代码段

> - 程序中可执行部分，直观为函数堆叠组成
> - 特殊数据放到代码段
> 	- char *p = "linux";
> 	- const修饰的变量

### 数据段（.data）

> - 别名：数据区、静态数据区、静态区
> - 直观理解为C语言中的全局变量才是程序的数据
> - 具体为：显示初始化为非零的全局变量和静态全局变量都在数据段

### bss段

> - 初始化为0的数据段
> - 注意：未显示初始化全局变量值默认0
> - 具体为：未初始化或显示初始化为0的全局变量

### 总结 -- 变量和常量使用内存情况

> - 相同点：为程序提供内存，为程序定义变量
> - 不同点：
> 	- 栈：对应局部变量（自动分配和回收）（临时的公交）
> 	- 堆：独立的，由程序员malloc（）和free（）（借的共享单车）
> 	- 数据段：对应全局变量和静态局部变量
> - 获取内存机制的依据
> 	- 栈：临时使用，出了函数就不用。
> - 堆和数据段：几乎可完全替换。
> 	- 不同点：生命周期不同
> 		- 堆是阶段性的（从malloc（）到free（）） -- 租房
> 		- 数据段全程性，伴随程序开始到结束  -- 买房
