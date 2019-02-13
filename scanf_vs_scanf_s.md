Unlike scanf and wscanf, scanf_s and wscanf_s require the buffer size to be specified 
for all input parameters of type 

*c, C, s, S, or [.*

The buffer size in characters is passed as an __additional parameter__ immediately following the pointer to the buffer or variable. 

For example, if reading a string, the buffer size for that string is passed as follows:

```cpp
char s[10];
scanf_s("%9s", s, 10); // buffer size is 10, width specification is 9
```
