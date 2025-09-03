
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

# Напишите рекурсивную функцию calculatePower, которая вычисляет степень числа. Функция calculatePower должна принимать два аргумента: число base и целое число exponent. Она должна возвращать результат возведения числа base в степень exponent.

Входные данные

Число base, которое может быть целым или с плавающей точкой.

Целое число exponent, которое может быть положительным, отрицательным или равным нулю.

Выходные данные

Число, представляющее результат возведения числа base в степень exponent с точностью 2 знака.

## Python
```
inp = input().split()
base, exponent = float(inp[0]), int(inp[1])

def calculatePower(base, exponent):
    if exponent > 0:
        return base * calculatePower(base, exponent-1)
    elif exponent == 0:
        return 1.0
    else:
        return calculatePower(base, exponent+1) / base

print("{:.2f}".format(calculatePower(base, exponent)))
```

## Java
```
import java.util.Scanner;

class Alg {

    public static double calculatePower(double base, int exponent){
        if(exponent > 0)
            return base * calculatePower(base, exponent-1);
        else if(exponent == 0)
            return 1.0;
        else 
            return calculatePower(base, exponent+1) / base;
    }

    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        double base = sc.nextDouble();
        int exponent = sc.nextInt();
        System.out.printf("%.2f", calculatePower(base, exponent));
    }
}
```

## Kotlin
```
import java.util.Scanner

fun calculatePower(base: Double, exponent: Int): Double {
    if(exponent > 0)
        return base * calculatePower(base, exponent - 1)
    else if(exponent == 0)
        return 1.0
    else
        return calculatePower(base, exponent + 1) / base
}

fun main(){
    val scanner = Scanner(System.`in`)
    var base = scanner.nextDouble()
    var exponent = scanner.nextInt()
    
    println("%.2f".format(calculatePower(base, exponent)))
    
}
```

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
