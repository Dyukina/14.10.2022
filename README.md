# 14.10.2022
## 1. Count the number of divisors of a positive integer n.

Random tests go up to n = 500000.
___
### Мое рещение
```java

public class FindDivisor {

public long numberOfDivisors(int n) {
long counter = 0;
for(int i=1; i<=n; i++){
if(n % i == 0){
counter++;
}
}
return counter;
}
}
```

### Понравившееся решение
```java
import java.util.stream.IntStream;
public class FindDivisor {
public long numberOfDivisors(int n) {
return IntStream.range(1, n+1).filter(i -> n%i==0).count();
}
}
```
## 2. Find the minimum number of jumps to go from start to finish
[Task link](https://www.codewars.com/kata/62c93765cef6f10030dfa92b/train/java)
### Мое рещение
```java

public class Kata
{
public static int solution(int start, int finish)
{
int delta = finish - start;
return delta / 3 + delta % 3;
}
}
```

### Понравившееся решение
```java

public class Kata
{
public static int solution(int start, int finish)
{
int diff = (finish - start);
return diff/3 + diff % 3;
}
}
``` 
