Задание реализовано через docker-compose c использованием собственных собранных
образов размещенных на dockerhub https://hub.docker.com/repositories/zotowa

Запуск осуществляется командой docker-compose up -d

Вход в django http://<ваш_IP>:8000/

Админка доступна по адресу http://<ваш_IP>:8000/admin

Так как БД не переносилась в образы,
необходимо зайти в контейнер django-e410
используя команду docker exec -it django-e410 /bin/sh

и создать пользователя командой:
python manage.py createsuperuser

имя пользователя / admin
пароль / admin
почтовый адрес пустой

контейнер nginx запускается на 80 порту и выводит измененную начальную страницу     
