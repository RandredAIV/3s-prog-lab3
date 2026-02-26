как запускать чекать в readme в файлах лабы

g++ на C++ делать в папке tests, остальные команды просто в папке Lab3

g++ test.cpp -lgtest -lgtest_main -pthread -std=c++17 -o test_res

make

make coverage

cd out

xdg-open index.html


на go всё целиком

go run main.go

cd hashtable

go test -v -coverprofile=cover.out

go tool cover -html=cover.out -o cover.html

xdg-open cover.html
