# gallery
### Плотформа для галлереи фотографий
Можно опубликовать свои фотографии и добавить в избранное те фотографии которые вам понравились
### Запуск проекта локально.
##### Для того чтобы запустить проект локально, нужно склонировать проект с гита
``` 
$ git clone git@github.com:AlibekBeket/controlwork_9_alibek_beket.git 
```
##### После нужно зайти в файл репозитория
``` 
$ cd /{имя репозитория}
```
##### Создаем виртуальное окружение
``` 
$ virtualenv venv
```
##### Активировать его
``` 
$ . venv/bin/activate
```
##### Установить пакеты зависимостей
``` 
$ pip install -r requirements.txt
```
##### Создать базу данных
Через терминал или pgAdmin4 создат базу данных, затем изменить в settings.py название базы и пароль(который вы установили)
##### Сделать миграцию
``` 
$ ./manage.py migrate
```
##### Из фикстур взять все данные
``` 
$ ./manage.py loaddata auth.json dump.json
```
##### Также нужно установить csrftoken для api
``` 
Заходите через постман на путь http://127.0.0.1:8000/api/token/
method: GET
Капируете его и вставляете в headers
В таблице key вставляете X-CSRFToken, value - код из cookies с поля value
```
##### Теперь можно запустить программу
``` 
$ ./manage.py runserver
```
