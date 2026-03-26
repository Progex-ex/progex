Добавялем в конфиг контейнера две строки через команду  nano /etc/pve/lxc/105.conf (меняем номер контейнера)

lxc.cgroup2.devices.allow: c 10:200 rwm

lxc.mount.entry: /dev/net dev/net none bind,create=dir


Pritunl Server

1. Склонировать репозиторий: git clone https://github.com/Progex-ex/progex.git
2. Перейти в папку проекта: cd pritunl
3. Запустить сборку образа: docker compose build --no-cache
4. Запустить контейнеры: docker compose up -d
5. Сбросить пароль пользователя pritunl: docker compose exec -i pritunl pritunl default-password
