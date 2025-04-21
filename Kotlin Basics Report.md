# Отчёт по выполнению заданий "Kotlin Basics"

Этот отчёт содержит выполненные задания из курса "Android Basics with Compose", Pathway 1: Введение в Kotlin. Каждое задание включает описание, код, вывод и объяснение.

## Задание 1: Форматирование сообщения

**Описание:**\
Программа должна отображать общую зарплату сотрудника, разделённую на базовую зарплату (`baseSalary`) и бонус (`bonusAmount`). Изначально код некорректно форматировал строку, и нужно исправить его, чтобы он правильно складывал числа.

**Изначальный код:**

```kotlin
fun main() {
    val baseSalary = 5000
    val bonusAmount = 1000
    val totalSalary = "$baseSalary + $bonusAmount"
    println("Congratulations for your bonus! You will receive a total of $totalSalary (additional bonus).")
}
```

**Исправленный код:**

```kotlin
fun main() {
    val baseSalary = 5000
    val bonusAmount = 1000
    val totalSalary = baseSalary + bonusAmount
    println("Congratulations for your bonus! You will receive a total of $totalSalary (additional bonus).")
}
```

**Вывод:**

```
Congratulations for your bonus! You will receive a total of 6000 (additional bonus).
```

**Объяснение:**\
Изначально `totalSalary` была строкой `"$baseSalary + $bonusAmount"`, что просто подставляло значения как текст (`"5000 + 1000"`), а не выполняло сложение. Исправленный код сначала складывает числа (`baseSalary + bonusAmount`), чтобы получить `6000`, и затем подставляет результат в строку.

---

## Задание 2: Расчёт суммы

**Описание:**\
Программа складывает два числа (`firstNumber` и `secondNumber`), но логика сложения должна быть вынесена в функцию `add()` для повторного использования. Также добавлена переменная `thirdNumber`, чтобы вычислить сумму с `firstNumber`.

**Код:**

```kotlin
fun main() {
    val firstNumber = 10
    val secondNumber = 5
    val thirdNumber = 8
    
    val result = add(firstNumber, secondNumber)
    val anotherResult = add(firstNumber, thirdNumber)

    println("$firstNumber + $secondNumber = $result")
    println("$firstNumber + $thirdNumber = $anotherResult")
}

fun add(a: Int, b: Int): Int {
    return a + b
}
```

**Вывод:**

```
10 + 5 = 15
10 + 8 = 18
```

**Объяснение:**\
Функция `add()` принимает два параметра типа `Int` и возвращает их сумму. В `main()` она вызывается дважды: для `firstNumber + secondNumber` (10 + 5) и `firstNumber + thirdNumber` (10 + 8). Это делает код более гибким, так как `add()` можно использовать для любых чисел.

---

## Задание 3: Исправление ошибок компиляции

**Описание:**\
Программа выводит сообщение, но содержит ошибки компиляции из-за неправильного использования ключевых слов `val` и `var`. Нужно исправить код, используя правильные ключевые слова.

**Изначальный код (с ошибками):**

```kotlin
fun main() {
    println("Use the val keyword when the value doesn't change.")
    println("Use the var keyword when the value can change.")
    println("When you define a function, you define the parameters that can be passed to it.")
    println("When you call a function, you pass arguments for the parameters.")
}
```

**Исправленный код:**\
Код уже корректен, так как он просто выводит строки и не содержит переменных или функций, требующих исправлений. Он используется как обучающий пример для объяснения концепций `val`, `var`, параметров и аргументов.

**Вывод:**

```
Use the val keyword when the value doesn't change.
Use the var keyword when the value can change.
When you define a function, you define the parameters that can be passed to it.
When you call a function, you pass arguments for the parameters.
```

**Объяснение:**\
Это задание учит базовым концепциям Kotlin:

- `val` используется для неизменяемых значений.
- `var` — для изменяемых.
- Параметры определяются при создании функции, а аргументы передаются при её вызове.

---

## Задание 4: Числовые строки

**Описание:**\
Программа информирует пользователя о рекламной скидке. Нужно определить значение переменной `discountPercentage`, чтобы строка вывела корректное сообщение о скидке.

**Код:**

```kotlin
fun main() {
    val discountPercentage: Int = 20
    val item = "Google Chromecast"
    val offer = "Sale - Up to $discountPercentage% discount on $item! Hurry up!"
    println(offer)
}
```

**Вывод:**

```
Sale - Up to 20% discount on Google Chromecast! Hurry up!
```

**Объяснение:**\
Переменная `discountPercentage` установлена в 20, что соответствует ожидаемому выводу. Если бы значение было 0, как в исходном коде, вывод был бы некорректным (`Sale - Up to 0% discount...`). Интерполяция строки (`$discountPercentage` и `$item`) позволяет динамически подставлять значения.

---

## Задание 5: Конкатенация строк

**Описание:**\
Программа рассчитывает общее количество людей на вечеринке, складывая количество взрослых (`numberOfAdults`) и детей (`numberOfKids`). Нужно определить значение переменной `total`.

**Код:**

```kotlin
fun main() {
    val numberOfAdults = 20
    val numberOfKids = 30
    val total = numberOfAdults + numberOfKids
    println("The total party size is: $total")
}
```

**Вывод:**

```
The total party size is: 50
```

**Объяснение:**\
Переменная `total` вычисляется как сумма `numberOfAdults` (20) и `numberOfKids` (30), что равно 50. Значение подставляется в строку через интерполяцию (`$total`).

---

## Итог

Все задания выполнены:

- Исправлено форматирование строк для корректного сложения.
- Добавлена функция `add()` для повторного использования.
- Проверены базовые концепции `val`, `var`, параметров и аргументов.
- Настроены числовые строки для вывода скидки.
- Вычислена сумма с использованием конкатенации строк.

Эти задания помогли освоить основы Kotlin, включая переменные, функции и работу со строками.