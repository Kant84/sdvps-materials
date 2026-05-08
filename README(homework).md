# Домашнее задание «Что такое DevOps. CI/CD»
## Выполнил: Андрей Санакин

### Задание 1: Freestyle Project
- Создан проект `go-test-build` в Jenkins
- Подключен репозиторий https://github.com/Kant84/sdvps-materials.git
- Выполняются: `go test .` и `docker build . -t hello-world:v$BUILD_NUMBER`
- Статус: SUCCESS

### Задание 2: Pipeline
- Создан проект `go-test-pipeline` в Jenkins
- Declarative pipeline с этапами: Git → Test → Build
- Статус: SUCCESS

### Задание 3: Nexus + бинарный файл
- Установлен Nexus на http://192.168.101.146:8081
- Создан raw-hosted репозиторий `go-binaries`
- Pipeline модифицирован: сборка бинарного файла `CGO_ENABLED=0 GOOS=linux go build`
- Загрузка в Nexus через `curl`
- Файл `app-v3` успешно загружен

### Задание 4*: Версионирование
- Используется переменная `BUILD_NUMBER`
- Файлы именуются: `app-v1`, `app-v2`, `app-v3`...
