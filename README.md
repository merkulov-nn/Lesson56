# Lesson56
Домашнее задание

разворачиваем сетевую лабораторию
Описание/Пошаговая инструкция выполнения домашнего задания:

Для выполнения домашнего задания используйте методичку
https://docs.google.com/document/d/1XtCmYJYPKwoMDjwiTskALvYLZaE4I49g/edit?usp=share_link&ouid=104106368295333385634&rtpof=true&sd=true

Что нужно сделать?
otus-linux

Vagrantfile - для стенда урока 9 - Network
Дано

https://github.com/erlong15/otus-linux/tree/network
(ветка network)

Vagrantfile с начальным построением сети

    inetRouter
    
    centralRouter
    
    centralServer
    
    тестировалось на virtualbox
    
    Планируемая архитектура
    
    построить следующую архитектуру
    
    Сеть office1
    
    192.168.2.0/26 - dev
    
    192.168.2.64/26 - test servers
    
    192.168.2.128/26 - managers
    
    192.168.2.192/26 - office hardware
    
    Сеть office2
    
    192.168.1.0/25 - dev
    
    192.168.1.128/26 - test servers
    
    192.168.1.192/26 - office hardware
    
    Сеть central
    
    192.168.0.0/28 - directors
    
    192.168.0.32/28 - office hardware
    
    192.168.0.64/26 - wifi
    ```
    Office1 ---\
    ----> Central --IRouter --> internet
    Office2----/
    ```
    
    Итого должны получится следующие сервера
    inetRouter
    centralRouter
    office1Router
    office2Router
    centralServer
    office1Server
    office2Server
    
    Теоретическая часть
    
    Найти свободные подсети
    
    Посчитать сколько узлов в каждой подсети, включая свободные
    
    Указать broadcast адрес для каждой подсети
    
    проверить нет ли ошибок при разбиении
    
    Практическая часть
    
    Соединить офисы в сеть согласно схеме и настроить роутинг
    
    Все сервера и роутеры должны ходить в инет черз inetRouter
    
    Все сервера должны видеть друг друга
    
    у всех новых серверов отключить дефолт на нат (eth0), который вагрант поднимает для связи
    
    при нехватке сетевых интервейсов добавить по несколько адресов на интерфейс
