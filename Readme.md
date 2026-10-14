# Исходники сайта [docs.llmops.ru](https://docs.llmops.ru)

Запустить docs.llmops.ru на своем хосте с использованием docker контейнера:

    $ docker run -i -t -p 80:80 --name docs.llmops.ru marley/docs.llmops.ru

<br/>

### Как сервис

    # vi /etc/systemd/system/docs.llmops.ru.service

вставить содержимое файла docs.llmops.ru.service

    # systemctl enable docs.llmops.ru.service
    # systemctl start  docs.llmops.ru.service
    # systemctl status docs.llmops.ru.service

http://localhost:4006

<br/>

### Вариант для внесения изменений

Инсталлируете docker и docker-compose, далее:

    $ cd ~
    $ mkdir -p docs.llmops.ru && cd docs.llmops.ru
    $ git clone --depth=1 https://github.com/webmakaka/docs.llmops.ru.git .
    $ docker-compose up

<br/>

Остается в браузере подключиться к localhost:80
