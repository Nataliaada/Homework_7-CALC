

**Задача: написать программу "калькулятор" для работы с рациональными числами, организовать меню, добавив систему логирования**
 
*Программа состоит из следующих модулей:*

Модуль main (запуск программы)

Модуль interface (графический интерфейс в виде калькулятора)

Модуль rational (модуль вычисления

Модуль logger (осуществляет запись введенных операций)

Схема взаимодействия модулей: scema_moduls.jpg


**Описание модулей**


**Запуск программы (main)**

Через этот модуль запускается модуль графического интерфейса.

**Графический интерфейс (interface)**

Представляет собой калькулятор с полем для ввода выражения и конпками цифр (0-9), знаков арифметических действий (+, -, *, /), знаков скобок, копоки удаления всей записи (С) и удаления последнего символа, а также кнопки для нахождения значения выражения. Модуль содержит функцииб которые запускаются при нажатии кнопок. При нажатии пользователем кнопки "Вычислить" модуль обращается к вычислительному модулю, потом записывает операцию через модуль логирования в файл log.csr.

**Вычислительный модуль**

Выполняет 4 арифметических операций:  
 сложение 
 вычитание
 умножение 
 деление

Модуль принимает выражение из поля ввода калькулятора как строку. Переводит данную строку в список строк, содержащий как операции так и числа. Далее находит все скобки и выполняет операции в них, согласно порядку выполнения арифметичексих операций. При выполнении оперции происходит замена трех элементов списка на один элемент, который является результатом выполнения операции. В результате остается один элемент, который и является ответом. Данный результат передается обратно в графический модуль, который выводит его в поле ввода калькулятора.

**Модуль записи операций**

После вычисления значения выражения в файл log.csr дата вычисления, выражение, которое ввел пользователь и результат вычислений.