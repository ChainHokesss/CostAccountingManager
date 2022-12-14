# Требования к проекту
---

# Содержание
1 [Введение](#intro)  
1.1 [Назначение](#appointment)  
2 [Требования пользователя](#user_requirements)  
2.1 [Программные интерфейсы](#software_interfaces)
2.2 [Характеристики пользователей](#user_specifications)  
2.2.1 [Классы пользователей](#user_classes)  
2.2.2 [Целевая аудитория](#target_audience)                                   
3 [Системные требования](#system_requirements)  
3.1 [Функциональные требования](#functional_requirements)  
3.2 [Нефункциональные требования](#non-functional_requirements)  

<a name="intro"/>

# 1 Введение

<a name="appointment"/>

## 1.1 Назначение

В этом документе описаны функциональные и нефункциональные требования к приложению «СA Manager API» для web. Проект представляет собой серверную часть приложения для учета расходов, с возможностью групировать транзакции по различным категориям, а также создавать собственные категории.

<a name="user_requirements"/>

# 2 Требования пользователя

<a name="software_interfaces"/>

## 2.1 Программные интерфейсы
Проект включает в себя только серверную часть. Сервер должен быть реализован с использованием современных бэкенд технологий, а именно такого фреймворка как Django. Сервер должен осуществлять активное взаимодействие с базой данных PostgresQL для хранения всей информации приложения, включая информацию о пользователях, транзакциях, категориях. Также сервер должен иметь хорошую документацию для упрощения работы фронтенд разработчика. Документация должна быть сделана с помощью Swagger.

### 2.2 Характеристики пользователей

<a name="user_classes"/>

#### 2.2.1 Классификация пользователей

В приложении существуют 3 группы полезователей:

1. Обычные пользователи
2. Админ

Обычные пользователи - пользователи, которые зарегистрировались и авторизировались в приложении. Они могут вести учет своих расходов, создавать категории и просматривать свою статистику.
Супер-админ - пользователь, который наделен особыми правами через серверскую консоль. Они имеют все права обычного пользователя, а также могут менять права других пользователей удалять и изменят их.

<a name="target_audience"/>

#### 2.2.2 Целевая аудитория

Данное приложение ориентировано на обычных пользователей, которые желают вести учет своих расходов.

<a name="system_requirements"/>

## 3. Системные требования

<a name="functional_requirements"/>

### 3.1 Функциональные требования

Должны быть реализованы следующие возможности:
1. Регистрация пользователей
2. Авторизация пользователей
3. Транзакции пользователя - CRUD
    1. Списание баланса
    2. Начисление баланса
    3. фильтрация и сортировка транзакций по времени, сумме и дате
4. Категории пользователя - CRUD
   1. Создание своей категории
   2. Удаление и изменение стандартных категорий
5. Просмотр профиля пользователя
6. Просмотр статистики пользователя
   1. отправка статистики в ответ на запрос
   2. отправка статистики на почту

<a name="non-functional_requirements"/>

### 3.2 Нефункциональные требования

1. Версия Django
2. Версия Django Rest Framework
3. Версия Celery
4. Версия PostgreSQl
5. Разертка проекта может осуществляться на удаленном хостинг сервисе Heroku на бесплатной осоновеы
