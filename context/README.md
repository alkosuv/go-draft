# Context


## Когда использовать context?

### WithTimeout / WithDeadline / CancelFunc / WithCancel / WithCancelCause
- Если Go routine'а может зависнуть на долго, то лучше использовать context для прирывания работы  Go routine'ы.
- Если метод/функция ходит по сети, то такой первым параметром надо передавать context. Это необходимо для прирывания 
долгих запросов во избижания зависания приложения.

### WithValue

- В редких случая можено испольховать. Чаще всего если нет легального способа передать данные через сторонний пакет


## Link

- [Package context](https://pkg.go.dev/context)
- [Разбираемся с контекстами в #Go / туториал по context.Context в #Golang](https://www.youtube.com/watch?v=Fjkckov4F38)