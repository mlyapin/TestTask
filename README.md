# TestTask
> Упс, забыл проверять наличие директории `testTask/storage`, которую использую для хранения данных.
  Попрошу Вас или создать её, или в `testTask/saver/saver.go` изменить две соответствующие константы :)
## Структура
* _testTask/data_     - пакет, содержащий структуры, обрабатываемые сервисами.
* _testTask/receiver_ - 1-й микросервис: ожидает json, разбивает на две части, отправляет второму микросервису.
* _testTask/saver_    - 2-й микросервис: ожидает данные, записывает их в соответствующее расположение.
* _testTask/shared_   - пакет, содержащий стуктуры, методы и функции, использующиеся в обоих микросервисах.

## Зависимости
* [go-sqlite3](https://github.com/mattn/go-sqlite3)

## Endpoint'ы
### testTask/receiver
* `http://localhost:8081/message` - HTTP-метод: "PUT", В теле ожидает json, отражающий `testTask/data/message.go`
