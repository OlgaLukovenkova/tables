# Электронная таблица
## Описание
_Обучающий проект_. Реализует ограниченный фукнционал электронных таблиц. В ячейки можно вводить
- строки,
- числа (целые и с плавающей точкой),
- формулы, задающие операции над числами,
- формулы со ссылками на значения в др. ячейках.

## Модули
`Formula.g4` - описание грамматики формулы для ANTRL.

`FormulaAST` - содержит класс синтаксического дерева формулы, функция `ParseFormulaAST` преобразует строковое представление формулы в экземпляр класса. Класс использует специальную программу ANTRL для генерации кода лексического и синтаксического анализаторов.

`cell` - класс ячейки таблицы.

`common` - описания интерфейсов ячейки и листа, а также позиции ячейки в листе (ее адреса), размера заполненной области листа, класса ошибок, возникающих при вычислениях, и возможных исключений.

`formula` - описание интерфейса формулы и его реализация.

`sheet` - класс листа.

`test_runner_p.h` - фреймворк для запуска unit-тестов.

## Инструкция по запуску
Для запуска необходимо
- скачать antlr-4.13.0-complete.jar c сайта [ANTRL](https://www.antlr.org/download.html) (ANTLR tool and Java Target).
- скачать архив antlr4-cpp-runtime*.zip с сайта [ANTRL](https://www.antlr.org/download.html) (раздел С++ Target).
- выстроить следующую структуру проекта

```spreadsheet/  
├── antlr4_runtime/  
│   └── Содержимое архива antlr4-cpp-runtime*.zip.  
├── build/  
├── antlr-4.13.0-complete.jar  
├── CMakeLists.txt  
├── FindANTLR.cmake  
├── Formula.g4  
├── Остальные файлы проекта  
└── ...
```

## Системные требования
C++17
