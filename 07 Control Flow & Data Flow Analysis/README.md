# Control Flow Analysis & Data Flow Analysis

based on the lecture by V. Krishna Nandivada from IIT Madras

Code optimization requires that the compiler has a global understanding of how programs use the available resources.

It has to understand the control flows in the program and how the data is manipulated (data-flow analysis)

Control-flow analysis: flow of control within each procedure.

Data-flow analysis: how the data is manipulated in the program.

## Control Flow Analysis

Control-flow analysis discovers the flow of control within a procedure
(e.g., builds a CFG, identifies loops)

```sh
a := 0
b := a * b
L1: c := b/d
if c < x goto L2
e := b / c
f := e + 1
L2: g := f
h := t - g
if e > 0 goto L3
goto L1
L3: return
```
### C Version

```c
#include <stdio.h>

```

## Data Flow Analysis

Data-flow analysis derives information about the dynamic
behavior of a program by only examining the static code

(ie, How many registers do we need for the program )

```c

#include <stdio.h>

int main(){
    int a = 10;
    int b = 20;
    printf("The Sum is %d",a+b);
    return 0;
}