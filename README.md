# RU
# Юнит-тестирование абстрактных структур данных

## Описание
Проект покрывает юнит-тестами реализации абстрактных структур данных
на C++ (GoogleTest) и Go (testing). Включает генерацию HTML-отчётов
о покрытии кода тестами.

## Реализованные структуры и тесты
- Динамический массив — тесты инициализации, добавления, удаления элементов
- Односвязный список — тесты добавления, удаления, поиска
- Двусвязный список — тесты двунаправленного обхода, вставки и удаления
- Стек — тесты push/pop/peek операций
- Очередь — тесты enqueue/dequeue операций
- Хеш-таблица — тесты добавления, удаления, сохранения и загрузки из файла (C++ и Go)

## Структура файлов
### C++  
```
├── libs/  
│   ├── hash_table.h       # Хеш-таблица  
│   ├── listD.h            # Двусвязный список  
│   ├── listS.h            # Односвязный список  
│   ├── massive.h          # Динамический массив  
│   ├── queue.h            # Очередь  
│   ├── stack.h            # Стек  
│   └── includes.h         # Общие зависимости  
├── tests/  
│   └── test.cpp           # Юнит-тесты (GoogleTest)  
└── Makefile               # Сборка и генерация отчёта покрытия  
```
### Go  
└── GO/  
    ├── main.go                  # Точка входа  
    └── hashtable/  
        ├── hashtable.go         # Реализация хеш-таблицы  
        └── hashtable_test.go    # Юнит-тесты  

## Язык программирования
C++, Go

## Запуск

### C++ — запуск тестов (выполнять из папки tests/)
g++ test.cpp -lgtest -lgtest_main -pthread -std=c++17 -o test_res

### C++ — генерация HTML-отчёта о покрытии (выполнять из папки Lab3/)
make  
make coverage  
cd out  
xdg-open index.html  

### Go — запуск основной программы (выполнять из папки Lab3/)
go run main.go

### Go — запуск тестов и генерация HTML-отчёта о покрытии (выполнять из папки hashtable/)
go test -v -coverprofile=cover.out  
go tool cover -html=cover.out -o cover.html  
xdg-open cover.html  

---
# EN
# Unit Testing of Abstract Data Structures

## Description
The project covers unit testing of abstract data structure implementations
in C++ (GoogleTest) and Go (testing package). Includes HTML code coverage
report generation.

## Implemented Structures and Tests
- Dynamic Array — initialization, push, delete tests
- Singly Linked List — push, delete, search tests
- Doubly Linked List — bidirectional traversal, insert and delete tests
- Stack — push/pop/peek operation tests
- Queue — enqueue/dequeue operation tests
- Hash Table — insert, delete, save and load from file tests (C++ and Go)

## File Structure
### C++  
├── libs/  
│   ├── hash_table.h       # Hash table  
│   ├── listD.h            # Doubly linked list  
│   ├── listS.h            # Singly linked list  
│   ├── massive.h          # Dynamic array  
│   ├── queue.h            # Queue  
│   ├── stack.h            # Stack  
│   └── includes.h         # Common dependencies  
├── tests/  
│   └── test.cpp           # Unit tests (GoogleTest)  
└── Makefile               # Build and coverage report generation  

### Go  
└── GO/
    ├── main.go                  # Entry point  
    └── hashtable/  
        ├── hashtable.go         # Hash table implementation  
        └── hashtable_test.go    # Unit tests  

## Language
C++, Go

## How to Run

### C++ — run tests (execute from the tests/ directory)
g++ test.cpp -lgtest -lgtest_main -pthread -std=c++17 -o test_res  

### C++ — generate HTML coverage report (execute from the Lab3/ directory)
make  
make coverage  
cd out  
xdg-open index.html  

### Go — run main program (execute from the Lab3/ directory)
go run main.go  
  
### Go — run tests and generate HTML coverage report (execute from the hashtable/ directory)
go test -v -coverprofile=cover.out  
go tool cover -html=cover.out -o cover.html
xdg-open cover.html
