# ClienD-proxy
Скрипт для настройки proxy-серверов для Wireless@School на Linux

## Установка и запуск
### Дома (или в месте с нормальным интернетом)
0. Установить [NodeJS] (http://nodejs.org)
0. Скачать [последнюю версию] (https://github.com/atnartur/ClienD-proxy/releases) программы
0. В папке проекта выполнить в консоли ```npm install```

Для того, чтобы запустить программу в школе, скачайте [бинарный файл NodeJS] (https://nodejs.org/download/).

### В школе
0. Выполнить ```sudo nodejs start```
0. Ввести логин и пароль от edu.tatar.ru
0. Перезагрузить компьютер.

После этого через прокси будут работать браузер Google Chrome, менеджер пакетов apt, а также программы, запущенные из bash.

Программа протестирована на ноутбуке ICL RayBook SI152 с установленной Xubuntu 13.04.

## Документация

### Команды
- start - прописывает прокси-конфигурацию в файлы.
- remove - убирает блок прокси-конфигурации из файлов. Важно: указывать тот же логин и пароль, что и были указаны при выполнении команды start.
- check - проверяет наличие блоков прокси-конфигурации. Важно: указывать тот же логин и пароль, что и были указаны при выполнении команды start.

### Затрагиваемые файлы
- ```/etc/apt/apt.conf.d/00cliendproxy``` (apt)
- ```~/.bashrc``` текущего пользователя
- ```/usr/bin/google-chrome``` (Google Chrome).

Блок прокси-конфигурации начинается и заканчивается комментарием ```# ClienD proxy```.

### Конфигурация
Параметры прокси сервера указываются в файле config.json.

## Автор
Оригинальный код написан [Атнагуловым Артуром] (http://atnartur.ru) <artur@clienddev.ru> при поддержке [ClienDDev team] (http://clienddev.ru) под лицензией MIT.

[Сообщить о проблеме] (https://github.com/atnartur/ClienD-proxy/issues)
