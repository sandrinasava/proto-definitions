# Proto Definitions
## Описание
Здесь находятся определения протоколов, используемых в проекте [cafe-services](https://github.com/sandrinasava/cafe-services). Эти определения необходимы для взаимодействия между микросервисами.
При изменении .proto, Workflow отправляет новые сгенерированные файлы в [go-proto-module](https://github.com/sandrinasava/go-proto-module)

## Мотивы вынесения .proto-файла и сгенерированного кода из [cafe-services](https://github.com/sandrinasava/cafe-services):

- ### Упрощение управления зависимостями:
   В микросервисах достаточно указать зависимость на go-proto-module, вместо того, чтобы хранить .proto-файлы и генерировать код непосредственно в каждом микросервисе.

- ### Упрощенная актуализация контракта:
   Достаточно изменить .proto в proto-definitions и обновить зависимости в проекте.
   В свою очередь Workflow в proto-definitions обновит информацию в go-proto-module.

