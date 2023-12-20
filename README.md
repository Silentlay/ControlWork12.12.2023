# Введение

```text
Данная программа решает задачу, которая из имеющегося массива строк формирует новый массив из строк, длина которых меньше, либо равна 3 символам. Первоначальный массив можно ввести с клавиатуры, либо задать на старте выполнения алгоритма.
```

## ``Описание решения:``

### **1. Ввод пользователем:**

• Программа начинается с вывода на консоль приглашения: ``"Хотите ввести свой массив строк? (y/n)"``

• Пользователь вводит **ДА** или **НЕТ** в зависимости от того, хочет ли он ввести свой массив строк.

### **2. Обработка выбора пользователя:**

• Если пользователь вводит ``"y"``:

• Программа выводит на экран: ``"Введите строки. Для завершения ввода введите пустую строку:"``

• Затем программа ожидает ввода строк с клавиатуры. ``Считывание строк происходит в цикле, пока не будет введена пустая строка.``

• Введенные строки сохраняются во ``временный массив`` **"tempArray"**, предварительно заданного размера **100**.

• ``Создается новый массив`` **"originalArray"** с использованием только необходимого размера, который равен количеству введенных строк.

• Если пользователь вводит ``"n"``:

• ``Программа инициализирует массив`` **"originalArray"** значением по умолчанию: ``"{"Hello", "2", "world", ":-)"}".``

• **Выводится сообщение:** ``"Используется массив по умолчанию."``

• ``Если пользователь вводит что-то иное``, программа выводит сообщение об ошибке: ``"Неверный ввод. Введите "y" или "n"."``

### **3. Формирование нового массива:**

• ``Программа вызывает метод "FormatArray"``, который **принимает массив** ``"originalArray"``.

• В методе ``"FormatArray"`` **создается новый массив** ``"resultArray"``, предварительно заданного размера, и **переменная** ``"newSize"`` для отслеживания текущего размера нового массива.

• **Происходит итерация по элементам** ``"originalArray"``, и если длина строки меньше или равна 3 символам, она добавляется в ``"resultArray"``.

• Используется ``"Array.Resize"`` для создания окончательного массива с использованием только необходимого размера.

### **4. Вывод результатов:**

• Программа **выводит на экран исходный массив** ``"originalArray"`` и **новый массив**, полученный после обработки методом ``"FormatArray"``.

• Результат выводится в виде строк, где каждая строка окружена кавычками и разделена запятой.

### ``Например``

```c#
[“Hello”, “2”, “world”, “:-)”] → [“2”, “:-)”]
```

```c#
[“1234”, “1567”, “-2”, “computer science”] → [“-2”]
```

```c#
[“Russia”, “Denmark”, “Kazan”] → []
```
