# Otus Homework 13. Docker
### Цель домашнего задания
Разобраться с основами docker, с образом, эко системой docker в целом.
### Описание домашнего задания
- Установите [Docker](https://docs.docker.com/engine/install/ubuntu/) на хост машину 
- Установите [Docker Compose](https://docs.docker.com/compose/install/linux/#install-the-plugin-manually) - как плагин, или как отдельное приложение
- Создайте свой кастомный образ *nginx* на базе *alpine*. После запуска *nginx* должен отдавать кастомную страницу (достаточно изменить дефолтную страницу *nginx*)
- Определите разницу между контейнером и образом
- Вывод опишите в домашнем задании.
- Ответьте на вопрос: Можно ли в контейнере собрать ядро?
### Задание со звездочкой
- Написать Docker-compose для приложения Redmine, с использованием опции build.
- Добавить в базовый образ redmine любую кастомную тему оформления.
- Убедиться что после сборки новая тема доступна в настройках.
- Настроить вольюмы, для сохранения всей необходимой информации



## Выполнение
*Dockerfile* для выполнения задания находится в каталоге [1-nginx](https://github.com/nikitinya89/otus_hw13_docker/tree/main/1-nginx).

Сборка образа:
```bash
docker build -t some-nginx .
```
Запуск контейнера:
```bash
docker run -d -p 80:80 some-nginx
```
В результате получим запущенный контейнер с установленным *nginx* на базе образа *alpine*, который отдает кастомную страницу, доступную на хосте по адрес http://localhost

Также образ добавлен в **Docker Hub** и доступен по адресу  
https://hub.docker.com/r/nikitinya89/otus_hw13/tags

Команда для загрузки образа:
```bash
docker pull nikitinya89/otus_hw13:latest
```
