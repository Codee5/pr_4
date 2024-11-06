# pr_4_Пашенин
using MarkdownSharp;
using MarkdownSharp.Extensions.Mal
**1. Задачи на линейное программирование (без условных операторов и циклов)**

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
