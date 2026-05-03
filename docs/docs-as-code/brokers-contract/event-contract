# Event Contract: Course Events

## Назначение

Событие `Event` используется для уведомления других сервисов системы онлайн-обучения об изменениях сущности `Course`.

## Producer

`course-service`

## Consumers

Потенциальные потребители события:

- сервис поиска курсов
- сервис рекомендаций
- сервис уведомлений
- аналитический сервис

## Kafka topic

`course-events`

## Message format

Protocol Buffers `proto3`.

## Protobuf file

`proto/course_events.proto`

## Event structure

Сообщение `Event` содержит:

| Поле | Описание |
|---|---|
| `event_id` | Уникальный идентификатор события |
| `event_type` | Тип изменения курса |
| `created_time` | Дата и время создания события |
| `course` | Данные курса |

## Event types

| Значение | Описание |
|---|---|
| `COURSE_CREATED` | Курс создан |
| `COURSE_UPDATED` | Данные курса изменены |
| `COURSE_PUBLISHED` | Курс опубликован |
| `COURSE_ARCHIVED` | Курс архивирован |
| `COURSE_DELETED` | Курс удалён |

## Kafka key

В качестве Kafka key используется:

```text
course.id
