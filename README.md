
# Напишите рекурсивную функцию countDigits, которая вычисляет количество цифр в заданном целом числе. Функция countDigits должна принимать целое число n в качестве аргумента и возвращать количество цифр в числе n.

Входные данные

Целое число n, где n может быть как положительным, так и отрицательным.

Выходные данные

Целое число, представляющее количество цифр в числе n

## Python
```
n = int(input())

def countDigits(n, count = 0):
    if(n // 10 != 0):
        return countDigits(n // 10, count + 1)
    else:
        return count + 1

print(countDigits(abs(n)))
```

## Java
```
import java.util.Scanner;

class Alg {
    public static int countDigits(int n, int count){
        if (n / 10 != 0) 
            return countDigits(n / 10, count + 1);
        else
            return(count + 1);
    }
    
    public static void main(String[] args){ 
        Scanner sc = new Scanner(System.in); 
        int n = sc.nextInt(); 
        int count = 0;
        System.out.print(countDigits(n, 0));
            
        
    }
}
```

## Kotlin
```
import java.util.Scanner

fun countDigits(n: Int): Int {
    val absN = kotlin.math.abs(n)
    if (absN / 10 != 0)
        return 1 + countDigits(absN / 10)
    else
        return 1
}

fun main() {
    val scanner = Scanner(System.`in`)
    val n = scanner.nextInt()
    println(countDigits(n))
}
```

Задействуется  2 варианта разного решения на разных ЯП для лучшей практики




# Шаблон
## Python
```

```

## Java
```

```

## Kotlin
```

```
