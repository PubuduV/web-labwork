Изначально строка преобразуется в массив из символов операций и чисел с помощью arrayExp. Это нужно для того, чтобы проверить строку на правильность введенных данных (отсутствие недопустимых символов, наличие только пар скобок (открывающей и закрывающей), соответствие числа символов операций и операндов (операндов всегда на 1 больше чем количество операций, иначе выражение не имеет смысла)). Дальнейшие проверки (правильный порядок скобок и их позиция, количество операндов) выполняются при вычислении выражения, так как для них необходим рекурсивный подход.

Функция calc содержит функцию makeCalc, которая работает рекурсивно: она проходит по выражению слева направо и ожидает получить 
выражение, которым является последовательность из символа операции и двух операндов, при этом любой из операндов 
может являться выражением.

Если операндом является выражение, то вычисление текущего выражения приостанавливается и вызывается функция makeCalc, которая в конечном счете
вернет некоторое значение выражения в фунцию, которая ее вызывала. Вернется числовое значение, если выражение записано верно и нечисловое, если обнаружена ошибка, например (* 2 2 3) вызовет ошибку, так как внутри скобок есть лишний операнд, будет выведено соответствующее сообщение об ошибке: "There are extra or wrong values in the expression".

Функция печатает сообщение об ошибке, в качестве результата работы, либо выводит ответ.


Initially, the string is converted to an array of operation characters and numbers using arrayExp. This is necessary in order to check the string for the correctness of the entered data (the absence of invalid characters, the presence of only pairs of parentheses (opening and closing), the correspondence of the number of symbols of operations and operands (operands are always 1 more than the number of operations, otherwise the expression is meaningless)) ... Further checks (correct order of brackets and their position, number of operands) are performed when evaluating the expression, since they require a recursive approach.

The calc function contains the makeCalc function, which works recursively: it iterates over the expression from left to right and expects to receive
expression, which is a sequence of an operation symbol and two operands, with either of the operands
can be an expression.

If the operand is an expression, then the evaluation of the current expression is suspended and the makeCalc function is called, which ultimately
will return some value of the expression to the function that called it. A numeric value will be returned if the expression is written correctly and non-numeric. ".

The function prints an error message as a result of the work, or outputs the answer.
