<?php

// Функция для объединения двух массивов
function merge_arrays($array1, $array2) {
    return array_unique(array_merge($array1, $array2)); // Объединяет массивы и удаляет дубликаты
}

// Функция для вычисления чисел Фибоначчи до n
function fibonacci($n) {
    $fibonacci_numbers = [];
    $a = 0; // Первое число Фибоначчи
    $b = 1; // Второе число Фибоначчи

    for ($i = 0; $i < $n; $i++) {
        $fibonacci_numbers[] = $a; // Добавляем текущее число в массив
        $next = $a + $b; // Вычисляем следующее число
        $a = $b; // Сдвигаем числа
        $b = $next; // Обновляем второе число
    }

    return $fibonacci_numbers; // Возвращаем массив чисел Фибоначчи
}

// Пример использования
$array1 = [1, 2, 3, 4, 5];
$array2 = [4, 5, 6, 7, 8];
$merged = merge_arrays($array1, $array2); // Объединяем массивы

$fib_numbers = fibonacci(10); // Получаем первые 10 чисел Фибоначчи

print_r($merged); // Выводим объединённый массив
print_r($fib_numbers); // Выводим числа Фибоначчи
?>



