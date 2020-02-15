# CPE_getnextline_2019
My implementation of the getline function in C

# Subject
The goal of this project is to write a function that returns a read line from a file descriptor.  
If there are no more lines to return, or if there is an error during the reading, the function will come back
NULL.  
You must define a macro called READ_SIZE in your get_next_line.h file, which indicates the amount of
characters to be read for each read() call.  

- prototype : 
```c 
char *get_next_line(int fd);
```

# Example
```c
#include <stdlib.h>
#include <stdio.h>
#include "get_next_line.h"

int main(void)
{
  char *s = get_next_line(0);
  
  while (s) {
    puts(s);
    putchar('\n');
    free(s);
    s = get_next_line (0) ;
  }
  return (0) ;
}
```
