# Вычисления

Иногда недостаточно просто писать числа. Иногда вам нужны вычисления.  
Помните, что вы можете использовать больше двух чисел одновременно, `1+1+1+1` будет работать, как надо.

## Совет

When unexpected results happen in a calculation, it is very well possible that you used two different types.  
For example `13 % 6.5` returns 1, even though the correct result is 0. Why? ZenScript always performs its calculations with two variables of the same type. For this, it converts the 2nd Type to match the first one. In this example, the calculation performed was `13 % 6`, as the 2nd number (a double) was converted to match the first one (an Integer).

Always be careful about what two variable types you use and when in doubt, just use a print function to print the output to the log and confirm the results.

## Арифметические операторы

Я почти уверен, что вы уже их знаете, да?

| Знак | Присваивающий знак | Функция           | Пример |
| ---- | ------------------ | ----------------- | ------ |
| `+`  | `+=`               | Сложение          | 1+2    |
| `-`  | `-=`               | Вычитание         | 2-1    |
| `*`  | `*=`               | Умножение         | 1*1    |
| `/`  | `/=`               | Деление           | 2/2    |
| `%`  | `%=`               | Деление по модулю | 13 % 6 |

## Конкатенация

Приклеивает одно к другому.

```zenscript
//prints "Hello World"
print("Привет," ~ " " ~ "Мир");
```

## Результаты вычисления

Обычно вычисление выдает какой-то результат. Что с ним делать?

### Присваивание переменной

Есть два способа присвоить значение переменной:

```zenscript
var test = 0;

//Option 1:
//assigns test with the value 3 (1+2)
test = 1+2;

//Option 2:
//assigns test with 5 (3+2)
test = test + 2;

//Option 3:
//assigns test with 2 (5-3)
test -= 3;
```

Option 1 and 2 assign the return variable using the `=` token.  
This is probably the easiest way for beginners and the only way if you want to assign a variable not used in the calculation.

Option 3 assigns the variable before the `-=` with the result of a normal subtraction.  
All Operators on on this page have their respective assign tokens, check the table above.

### Использование результата по-другому

Вы всегда можете использовать результат вычисления в функции или условном выражении:

```zenscript
//выводит 4
print(3+1);

//удаляет рецепт элемента массива array[4]
recipes.remove(array[3+1]);

//
if(3+1 == 2*2) {print("Используется вычисление!")}
```