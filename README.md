**Домашнее задание**
Развертывание Graylog

**Цель:**
Научиться принимать логи в graylog и создавать на их основы стримы.


**Описание/Пошаговая инструкция выполнения домашнего задания:**
Для успешного выполнения ДЗ вам нужно сконфигурировать Graylog и отправку логов в него

На виртуальной машине установите любую open source CMS, которая включает в себя следующие компоненты: nginx, php-fpm, database (MySQL or Postgresql). Можно взять из предыдущих заданий;
На этой же VM установите graylog sidecar.
Установите на второй VM Graylog (server, opensearch, mongodb) и datapreper
Подключите установленный sidecar в graylog и настройте сбор и отправку логов nginx, php-fpm и базы данных, используя sidecar.
Разделите логи в разные стримы.

В качестве результата создайте репозиторий приложите конфиги datapreper, sidecar.

Приложите скриншот полученных данных отображенных в Graylog.

______________________________________________________________________________________________________

На одной ВМ (192.168.114.27) Развернуты контейнеры с Graylog, mongo, opensearch.
![vm-graylog](https://github.com/user-attachments/assets/04cf0501-e2c6-45b0-90f5-da776160195c)



На другой ВМ (192.168.114.125) Работают компоненты nginx, php-fpm, mariadb. Sidecar и filebeat собирает данные.

В Graylog, созданы стримы, настроен inputs, и применен grok для стрима с ngixn.

**Streams**
![streams](https://github.com/user-attachments/assets/3ae0e47b-2dc8-4668-ac1f-4c32d22c7e97)


**Inputs**

![inputs](https://github.com/user-attachments/assets/9dfca514-2ea7-499a-94e0-8417579d62ea)


**Grok**

![grok-nginx1](https://github.com/user-attachments/assets/c758e56d-5f2b-4ece-b323-50b077f66ad4)
![grok-nginx](https://github.com/user-attachments/assets/550ee4b3-8269-4e42-a256-4674d132e118)


**Sidecars**

![sidecars](https://github.com/user-attachments/assets/e1198019-d1b0-4f48-80eb-588e9b4f6371)
![sidecars1](https://github.com/user-attachments/assets/46d19adb-d0f7-4e61-99e5-5a466350895f)



**Search**

![stream-php-rpm](https://github.com/user-attachments/assets/3dcd2677-d5bf-4788-9b13-c2f2e27c0f0f)
![stream-nginx](https://github.com/user-attachments/assets/901dad15-bdd9-406b-9020-3ea8047c8acd)
![stream-mariadb](https://github.com/user-attachments/assets/03e1f451-1c5d-4230-9300-66598cf84480)






