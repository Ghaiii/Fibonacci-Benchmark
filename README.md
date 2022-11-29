# Fibonacci
The Fibonacci numbers may be defined by the recurrence relation F0 = 0 , F1 = 1 , and Fn = F(n − 1) + F(n − 2) for n > 1.

# Fibonacci Series Iterative Method

```c
int iterative(int x){
    int f1 = 0;
    int f2 = 1;
    int output;
    if(x == 0){
        return f1;
    }else if(x == 1){
        return f2;
    }else{
        for(int i = 2; i <= x; i++){
            output = f1+f2;
            f1 = f2;
            f2 = output;
        }
        return output;
    }
}
```
# Fibonacci Series using Recursive Method
``` c
int recursive(int x){
    if(x == 0){
        return 0;
    } else if(x == 1){
        return 1;
    } else{
        return recursive(x-1)+recursive(x-2); 
    }
}
```

### Runing:
```
gcc -o teslib.o -c teslib/mylib.c
gcc -o test.exe test.c teslib.o
./test.exe
```
Result is : 
The fibonacci number for 11 is 89
The fibonacci number for 11 is 89
The fibonacci number F(0) = 0 = 0
The fibonacci number F(1) = 1 = 1
The fibonacci number F(2) = 1 = 1
The fibonacci number F(3) = 2 = 2
The fibonacci number F(4) = 3 = 3
The fibonacci number F(5) = 5 = 5
The fibonacci number F(6) = 8 = 8
The fibonacci number F(7) = 13 = 13
The fibonacci number F(8) = 21 = 21
The fibonacci number F(9) = 34 = 34
The fibonacci number F(10) = 55 = 55
The fibonacci number F(11) = 89 = 89

### Time Complexity
- Run:
```
gcc -o timeiterative.exe timeiterative.c teslib.o
gcc -o timerecursive.exe timerecursive.c teslib.o
./timeiterative.exe
./timerecursive.exe
```
Output: 
![Space N = 1000] : 
![Ghaii_timerelative](https://user-images.githubusercontent.com/114584858/204622253-b10de8d0-5e85-4404-a275-0992d7edfdf1.png)

![Space N = 1000] : 
![GhaiiTimeIterative](https://user-images.githubusercontent.com/114584858/204622277-2c02fb72-3ce1-4bee-846a-5f5044484ead.png)

### Space Complexity
on this one i used 1000 for the input for the space complexity.
- Run:
```
gcc -o spacerecursive.exe spacerecursive.c teslib.o
gcc -o spaceiterative.exe spaceiterative.c teslib.o
./spaceiterative.exe
./spacerecursive.exe
```
and the out put is : ![Space N = 1000] ![GhaiiTaskManager](https://user-images.githubusercontent.com/114584858/204623525-dc69ebb1-20af-4609-a88f-a4d4afd3cafe.png)
In conclusion, approaching the fibonacci series iteratively is more effective less time wasted and less space taken.
