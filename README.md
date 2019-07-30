# xiao-go-learning
### go tips

1. 定义常量的时候，默认值写成0，Status_UnKnown = 0
1. golang里面内联函数可能影响benchmark的性能，可以使用//go:noinline避免它
1. 函数里面返回指针会造成内存逃逸，函数里面的变量分配在栈上直接回收不用gc效率高，逃逸的变量分配在堆上需要进行gc可能影响性能。
1. 使用github.com/pkg/errors包裹错误，传递错误的context信息
1. 使用切片前如果知道容量，最后预先就分配大小
1. 使用context.Context进行进程通信和上下文取消
1. 使用-race检查程序是否有竞态行为
1. 函数参数使用抽象的鸭子类型而不是使用具体类型，比如传递reader而不是文件名
1. 循环里面的变量，如果有go协程那边要么闭包作为参数传递要么重新赋值一个循环变量
1. for循环里面的switch和select跳出的是内层循环
1. 
