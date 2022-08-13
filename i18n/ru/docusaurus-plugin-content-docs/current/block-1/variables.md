---
sidebar_position: 3
id: variables
---
# Переменные
Не изменяя традициям — перейдём к изучению переменных и всего, что с этим связано.
Что такое переменная? **Переменная** — символ или набор символов, которые представляют из себя какую-то величину или значение.
Для чего они нужны? — для записи результатов ваших вычислений и их дальнейшего использования.
Например, вы сделали какую-то часть вычислений, записали результат в переменную и переиспользовали ваши вычисления позже. Для этого и существуют переменные!
#### Как создать переменную в Kotlin
Чтобы создать переменную в Kotlin, мы используем ключевое слово `var` (от англ. variable).
```kotlin
var [название]: [Тип] = [значение] 
```
Состоит из:
* Название переменной, как название любой другой сущности — должно быть уникальным, начинаться с маленькой буквы и не иметь пробелов. Если в переменной несколько слов, следующие слова начинаются с большой (этот вид записи называют *lower camel case*).
* Тип — сущность, что описывает наши данные и будет содержаться в переменной. Например, это может быть целое число (т.е `Int`) или же число с запятой (т. е. `Double`).
  Для того чтобы присвоить какое-то значение переменной, используется знак равно `=` (и никак иначе).  
  После объявления такой переменной её можно изменить следующим способом:
```kotlin
[название] = [новоеЗначение]
```
Данный тип переменной, может меняться (данный термин в программировании ещё называют *мутабельностью*, от англ. mutable — изменяемый).
Но, подождите-ка, а бывают переменные, что не меняются? Само же название кричит о том, что «я меняюсь!».
##### Неизменяемые переменные
Да, такие существуют. Существуют для того, чтобы записывать значения, которые не меняются (что логично).
Например, если вам нужно только разово сделать какое-то вычисление и убедиться, что вы нигде его случайно не поменяете (дабы не вызвать ошибки в работе нашей программы).
Запись ничем не отличается от изменяемой переменной, за исключением того, что для неизменяемых переменных мы используем ключевое слово `val`.
```kotlin
val [название]: [Тип] = [значение]
```
Подобный тип переменной стоит использовать всегда, за исключением ситуаций, где вам нужно менять значение. Это упростит код и избавит вас от некоторых проблем.
### Типы данных
С этим разобрались, а какие типы данных существуют? Из встроенных существуют следующие:
- **Int** — это целое число, что имеет ограничение в размере от `-2147483647` до `2147483647` (число ограничено 32-я битами).
- **Float** — это число с плавающей точкой (или число с запятой), что имеет такое же, как и *Int*, ограничение в виде 32-битной размерности (т.е числа до `340,282,346,638,528,860,000,000,000,000,000,000,000.000000`).
- **Long** — это тот же Int, однако имеет большую размерность в два раза (до `9,223,372,036,854,775,807`).
- **Double** — это тот же Float, но опять же, большей размерности (где-то $1.7 \cdot 10^{308}$).
- **String** — простой текст. Не имеет ограничений, кроме как в количестве RAM.
  Все эти типы можно записать следующим образом:
```kotlin
val integer: Int = 999
val long: Long = 999_999_999 // для простоты чтения подобных чисел, можно использовать '_'
val float: Float = 1.0f // добавляется 'f' для явного указания, что мы вводим флоат
val double: Double = 999.99
val string: String = "я строка"
```
Так же, существуют некоторые другие встроенные типы данных, но мы их пока рассматривать не будем.
### Умозаключение
Подведём итог с переменными:
- переменные делятся на два типа: изменяемые `var` и неизменяемые `val`.
- у переменных всегда есть название, которое должно начинаться с маленькой буквы, а последующие слова — с большой. Так же, оно должно быть уникальным.
- у переменных всегда есть тип — сущность, что описывает данные или набор данных (например числа).
- у переменных всегда есть какое-то значение указанного типа (сущности).
- бывают следующие типы данных: целые числа (`Int` и `Long`), числа с запятой (`Float` и `Double`) и строки (обычный текст, `String`).