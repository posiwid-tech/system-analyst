# Course Events Contract

Учебный проект по проектированию событийного контракта для системы онлайн-обучения.

## Описание

Сервис управления курсами публикует события в Apache Kafka при изменении сущности `Course`.

Контракт описан в формате Protocol Buffers `proto3`.

## Состав репозитория

- `course_events.proto` — protobuf-контракт события
- `event-contract.md` — описание Kafka-события и правил обработки

## Домен

Система онлайн-обучения.

## Сущность

`Course` — учебный курс.

## Поддерживаемые события

- `COURSE_CREATED`
- `COURSE_UPDATED`
- `COURSE_PUBLISHED`
- `COURSE_ARCHIVED`
- `COURSE_DELETED`

## Kafka

- Topic: `course-events`
- Message format: Protobuf
- Kafka key: `course.id`

## Правило выбора Kafka key

В качестве Kafka key используется `course.id`, чтобы все события по одному курсу попадали в одну partition Kafka и обрабатывались в правильном порядке.
