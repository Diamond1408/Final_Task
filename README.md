# Задача # 
Написать программу, которая из имеющегося массива строк формирует массив из строк, длина которых меньше либо равна 3 символа. Первоначальный массив можно ввести с клавиатуры, либо задать на старте выполнения алгоритма. При решении не рекомендуется пользоваться коллекциями, лучше обойтись исключительно массивами.

# Решение #

Изначальный массив задается с консоли и разбивается на массив строк с помощью метода [Split](https://learn.microsoft.com/en-us/dotnet/csharp/how-to/parse-strings-using-split). Для простоты в качетсве разделителя строк взят символ пробела. Основной алгоритм описан в функции [StringsBySize](StringsBySize.jpg). Функция принимает в качестве параметра массив строк и максимально допустимую длину для строки для универасльности решения, и возвращает массив строк. Для данной задачи второй параметр задается "3". Так как неизвеста какова будет длина результирующего массива, то создается новый массив нулевой длины. Затем осуществляется обход с помощью оператора [foreach](https://learn.microsoft.com/ru-ru/dotnet/csharp/programming-guide/arrays/using-foreach-with-arrays) по всем элементам заданного массива и проверяется длина каждого элемента. Если длина элемента удовлетворяет условию, то элемент добавляется в конец и заменяется результирующий массив новым. Для удобства вывода массива используется функция "PrintArray", которая в квадратных скобках последовательно выводит элементы массива через запятую.