# pr_4_Пашенин
**1. Задачи на линейное программирование (без условных операторов и циклов)**

```
№1
package main

import "fmt"

var result int
var b int
var a int

func main() {
	fmt.Scanln(&a)
	for a = a; a > 0; a = a / 10 {
		b = a % 10
		result = result + b
		fmt.Println("+", b)
	}
	fmt.Print(result)
}

№2

package main

import "fmt"

var grad float64

func main() {
	fmt.Scanln(&grad)
	grad = grad*1.8 + 32
	fmt.Print(grad)
}

№3

package main

import "fmt"

var arr [4]int

func main() {
	for i := 0; i < len(arr); i++ {
		fmt.Scan(&arr[i])
	}
	for i := 0; i < len(arr); i++ {
		arr[i] = arr[i] * 2
	}
	fmt.Println(arr)
}

№4

package main

import "fmt"

var str1 string
var str2 string

func main() {
	fmt.Scan(&str1)
	fmt.Scan(&str2)

	str1 = str1 + " " + str2

	fmt.Print(str1)
}

№5 

package main

import (
	"fmt"
	"math"
)

var a1 float64
var a2 float64
var b1 float64
var b2 float64

func main() {
	fmt.Scan(&a1)
	fmt.Scan(&a2)
	fmt.Scan(&b1)
	fmt.Scan(&b2)

	a1 = a2 - a1
	b1 = b2 - b1

	a1 = math.Sqrt(a1*a1 + b1*b1)

	fmt.Print(a1)
}
```

**2. Задачи с условным оператором**
```
№1
package main

import (
	"fmt"
)

func main() {
	var number int
	fmt.Print("Введите число: ")
	fmt.Scan(&number)

	if number%2 == 0 {
		fmt.Println("Четное")
	} else {
		fmt.Println("Нечетное")
	}
}

№2

package main

import (
	"fmt"
)

var a int

func main() {
	fmt.Scan(&a)

	if a%4 == 0 {
		fmt.Print("Год високосный")
	} else {
		fmt.Print("Год не високосный")
	}
}

№3

package main

import (
	"fmt"
)

var arr [3]int
var c int

func main() {
	for i := 0; i < 3; i++ {
		fmt.Scan(&arr[i])
		if c < arr[i] {
			c = arr[i]
		}
	}
	fmt.Print(c)
}

№4

package main

import (
	"fmt"
)

var a int

func main() {
	fmt.Scan(&a)
	if a > -1 && a < 13 {
		fmt.Print("Ребенок")
	} else if a > 12 && a < 18 {
		fmt.Print("Подросток")
	} else if a > 17 && a < 60 {
		fmt.Print("Взрослый")
	} else {
		fmt.Print("Пожилой")
	}
}

№5

package main

import (
	"fmt"
)

var a int

func main() {
	fmt.Scan(&a)
	if a%3 == 0 && a%5 == 0 {
		fmt.Print("Делится")
	} else {
		fmt.Print("Не делится")
	}
}
 ```
**3. Задачи на циклы**
```
№1
package main

import (
	"fmt"
)

func factorial(n int) int {
	if n == 0 {
		return 1
	}
	return n * factorial(n-1)
}

func main() {
	var n int
	fmt.Print("Введите число для вычисления факториала: ")
	fmt.Scan(&n)
	fmt.Println("Факториал:", factorial(n))
}

№2
package main

import (
	"fmt"
)

func fibonacci(n int) []int {
	series := make([]int, n)
	if n > 0 {
		series[0] = 0
	}
	if n > 1 {
		series[1] = 1
	}
	for i := 2; i < n; i++ {
		series[i] = series[i-1] + series[i-2]
	}
	return series
}

func main() {
	var n int
	fmt.Print("Введите количество чисел Фибоначчи: ")
	fmt.Scan(&n)
	fmt.Println("Первые", n, "чисел Фибоначчи:", fibonacci(n))
}

№3

package main

import (
	"fmt"
)

var arr [5]int
var arr_rev [5]int

func main() {
	for i := 0; i < 5; i++ {
		fmt.Scan(&arr[i])
		arr_rev[4-i] = arr[i]
	}
	fmt.Print(arr_rev)
}

№4

package main

import (
	"fmt"
)

var n int

func main() {
	fmt.Scan(&n)
	for i := 0; i < n; i++ {
		if i%2 != 0 && i%5 != 0 && i%7 != 0 || i == 2 || i == 5 || i == 7 {
			fmt.Print(i, " ")
		}
	}
}

№5

package main

import (
	"fmt"
)

var arr [5]int
var res int

func main() {
	for i := 0; i < 5; i++ {
		fmt.Scan(&arr[i])
		res = res + arr[i]
	}
	fmt.Print(res)
}
```
