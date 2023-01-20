# Prometheus

## Домашнее задание

Установка и настройка Prometheus, использование exporters, настройка алертов

## Цель

Установить и настроить Prometheus.
Результатом выполнения данного дз будет являться публичный репозиторий в системе контроля версий (Github, Gitlab, etc.) в котором будет находится Readme с описание выполненых действий. Файлы конфигурации prometheus и alertmanager должны находится в директории GAP-1.

## Описание

### Для выполнения данного домашнего задания вам потребуется выполнить следующие действия

1. На виртуальной машине установите любую open source CMS которая включает в себя следующие компоненты: nginx, php-fpm, database (MySQL or Postgresql)
2. На этой же виртуальной машине установите Prometheus exporters для сбора метрик со всех компонентов системы (начиная с VM и заканчивая DB, не забудьте про blackbox exporter который будет проверять доступность вашей CMS)
3. На этой же или дополнительной виртуальной машине установите Prometheus задачей которого будет раз в 5 секунд собирать метрики с экспортеров
4. На этой же или дополнительной виртуальной машине установите Alertmanager и сконфигурируйте его таким образом чтобы в случае недоступности какого либо компонента был отправлен alert с важность Critical в один из канал оповещений (канал оповещений на выбор: slack or telegram)

* Задание со звездочкой 1 (повышенная сложность) - на VM с установленной CMS слишком много “портов экспортеров торчит наружу” и они доступны всем, попробуй настроить доступ только по одному и добавить авторизацию
  * Если вы выполнили задание со звездочкой номер 1 то - добавить SSL =)