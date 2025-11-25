### Exercise 2.01

Create and run Kernighan and Ritchie’s famous “hello, world” program:

```
#include <stdio.h>

int main(void)
{
printf("hello, world\n");
}
```
Do you get a warning message from the compiler? If so, what’s needed to make it go away?

## Solution

Compiling the program produced no errors using gcc version 15.2.1. Here is the output of the run commands used. 
```  
$ gcc -O -pedantic -Wall -W -std=c99 1.c
$ ./a.out
hello, world

$ gcc -O -pedantic -Wall -W -std=c89 1.c

1.c: In function ‘main’:
1.c:6:1: warning: control reaches end of non-void function [-Wreturn-type]
```

This warning can be fixed by adding ```return 0;``` to the program in 1.c.











