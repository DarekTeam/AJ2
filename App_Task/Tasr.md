# Задание 1

1)   Используйте команды операционной системы Linux и создайте две новых директории – «Игрушки для школьников» и «Игрушки для дошколят»
2)   Создайте в директории «Игрушки для школьников» текстовые файлы - «Роботы», «Конструктор», «Настольные игры»
3)   Создайте в директории «Игрушки для дошколят» текстовые файлы «Мягкие игрушки», «Куклы», «Машинки»
4)   Объединить 2 директории в одну «Имя Игрушки»
5)   Переименовать директорию «Имя Игрушки» в «Игрушки»
6)   Просмотреть содержимое каталога «Игрушки».
7)   Установить и удалить snap-пакет. (Любой, какой хотите)
8)   Добавить произвольную задачу для выполнения каждые 3 минуты (Например, запись в текстовый файл чего-то или копирование из каталога А в каталог Б).

# 1)   Используйте команды операционной системы Linux и создайте две новых директории – «Игрушки для школьников» и «Игрушки для дошколят»

db@gb-linux:~/devel$ mkdir Игрушки_для_школьников
db@gb-linux:~/devel$ mkdir Игрушки_для_дошколят
db@gb-linux:~/devel$ ls -l
итого 8
drwxrwxr-x 2 dbgb dbgb 4096 лют  Игрушки_для_дошколят
drwxrwxr-x 2 dbgb dbgb 4096 лют  Игрушки_для_школьников

# 2)   Создайте в директории «Игрушки для школьников» текстовые файлы - «Роботы», «Конструктор», «Настольные игры»

db@gb-linux:~/devel$ cd Игрушки_для_школьников/
db@gb-linux:~/devel/Игрушки_для_школьников$ ll
итого 8
drwxrwxr-x 2 grafany grafany 4096 лют ./
drwxrwxr-x 4 grafany grafany 4096 лют ../
db@gb-linux:~/devel/Игрушки_для_школьников$
db@gb-linux:~/devel/Игрушки_для_школьников$ cat > Роботы
Роботы
db@gb-linux:~/devel/Игрушки_для_школьников$
db@gb-linux:~/devel/Игрушки_для_школьников$ echo "Конструктор" > Конструктор
db@gb-linux:~/devel/Игрушки_для_школьников$ cat > Настольные_игры
db@gb-linux:~/devel/Игрушки_для_школьников$
db@gb-linux:~/devel/Игрушки_для_школьников$ ll

drwxrwxr-x 2 dbgb dbgb 4096 лют  ./
drwxrwxr-x 4 dbgb dbgb 4096 лют ../
-rw-rw-r-- 1 dbgb dbgb   23 лют Конструктор
-rw-rw-r-- 1 dbgb dbgb    29 лют Настольные_игры
-rw-rw-r-- 1 dbgb dbgb   13 лют Роботы
db@gb-linux:~/devel/Игрушки_для_школьников$
db@gb-linux:~/devel/Игрушки_для_школьников$ cd ..
db@gb-linux:~/devel$ ll

drwxrwxr-x  4 dbgb dbgb 4096 лют  ./
drwxr-x--- 23 dbgb dbgb 4096 лют  ../
drwxrwxr-x  2 dbgb dbgb 4096 лют  Игрушки_для_дошколят/
drwxrwxr-x  2 dbgb dbgb 4096 лют  Игрушки_для_школьников/

# 3)   Создайте в директории «Игрушки для дошколят» текстовые файлы «Мягкие игрушки», «Куклы», «Машинки»

db@gb-linux:~/devel$ cd Игрушки_для_дошколят/
db@gb-linux:~/devel/Игрушки_для_дошколят$ touch Мягкие_игрушки Куклы Машинки
db@gb-linux:~/devel/Игрушки_для_дошколят$ ls
Куклы  Машинки  Мягкие_игрушки
db@gb-linux:~/devel/Игрушки_для_дошколят$ cd ..
db@gb-linux:~/devel$ ls
Игрушки_для_дошколят  Игрушки_для_школьников
db@gb-linux:~/devel$ mkdir Имя_Игрушки
db@gb-linux:~/devel$ tree

# 4)   Объединить 2 директории в одну «Имя Игрушки»

db@gb-linux:~/devel$ mv Игрушки_для_дошколят/   Игрушки_для_школьников/ Имя_Игрушки/
db@gb-linux:~/devel$ ls
Имя_Игрушки
db@gb-linux:~/devel$ tree

# 5)   Переименовать директорию «Имя Игрушки» в «Игрушки»

db@gb-linux:~/devel$ mv Имя_Игрушки/ Игрушки

# 6)   Просмотреть содержимое каталога «Игрушки».

db@gb-linux:~/devel$ tree -g


# 7)   Установить и удалить snap-пакет. (Любой, какой хотите)

db@gb-linux:~/devel$ sudo snap find
Поисковый запрос пуст. Но имеются некоторые snap-пакеты, которые могут вас заинтересовать:

Название     Версия                            Издатель               Примечание  Описание
jami         20230130.1037.1b9159ac            sfljami                -           Privacy-oriented voice, video, chat, and conference platform and SIP phone
krita        5.1.1                             krita✓                 -           Digital Painting, Creative Freedom
thunderbird  102.8.0-2                         canonical✓             -           Mozilla Thunderbird email application
notepadqq    1.4.8                             danieleds              -           A Notepad++-like editor for Linux.
postman      10.10.9                           postman-inc✓           -           API Development Environment
mailspring   1.10.8                            foundry376✓            -           The best email app for people and teams at work
spotify      1.1.84.716.gc5f8b819              spotify✓               -           Music for everyone
slack        4.29.149                          slack✓                 -           Team communication for the 21st century.
foobar2000   1.6.16                            mmtrt                  -           foobar2000 is an advanced freeware audio player.
gimp         2.10.30                           snapcrafters           -           GNU Image Manipulation Program
hugo         0.110.0                           hugo-authors           -           Fast and Flexible Static Site Generator
inkscape     1.2.2-732a01da63-2022-12-09-cust  inkscape✓              -           Vector Graphics Editor
juju         2.9.38                            canonical✓             classic     Juju - a model-driven operator lifecycle manager for K8s and machines
skype        8.94.0.426                        skype✓                 -           One Skype for all your devices. New features. New look. All Skype.
litteris     master                            raibtoffoletto         -           Penpal Correspondence Organized
musescore    3.6.2                             musescore✓             -           Create, play and print beautiful sheet music.
newsboat     r2.30.1                           minoru                 -           An RSS/Atom feed reader for text terminals
qownnotes    23.2.5                            pbek                   -           Plain-text file markdown note taking with Nextcloud/ownCloud integration
retroarch    1.14.0                            libretro               -           RetroArch is the official reference frontend for the libretro API.
audacity     3.1.3                             diddledani✪            -           Audio software for multi-track recording and editing
bitwarden    2023.2.0                          bitwarden✓             -           Bitwarden
obs-studio   27.1.3                            snapcrafters           -           Free and open source software for live streaming and screen recording
gitkraken    9.1.1                             gitkraken✓             classic     For repo management, in-app code editing & issue tracking.
keepassxc    2.7.4                             keepassxreboot         -           Community-driven port of the Windows application “KeePass Password Safe”
vlc          3.0.18                            videolan✓              -           The ultimate media player
powershell   7.3.2                             microsoft-powershell✓  classic     PowerShell for every system!

Введите поисковый запрос так, чтобы результаты поиска были наиболее точны.
db@gb-linux:~/devel$ snap info powershell
name:      powershell
summary:   PowerShell for every system!
publisher: Microsoft PowerShell✓
store-url: https://snapcraft.io/powershell
contact:   https://github.com/powershell/powershell
license:   MIT
description: |
PowerShell is an automation and configuration management platform.
It consists of a cross-platform (Windows, Linux, and macOS)
command-line shell and associated scripting language.

See https://docs.microsoft.com/powershell/scripting/powershell-support-lifecycle for support
details.
snap-id: JSNnoJl3EqkMuWoy5Dgq8PMqZ0uNcpie
channels:
latest/stable:    7.3.2 2023-01-25 (229) 74MB classic
latest/candidate: ↑
latest/beta:      ↑
latest/edge:      ↑
lts/stable:       7.2.9 2023-01-25 (228) 72MB classic
lts/candidate:    7.2.8 2022-12-13 (227) 71MB classic
lts/beta:         7.2.8 2022-12-13 (227) 71MB classic
lts/edge:         7.2.8 2022-12-13 (227) 71MB classic
db@gb-linux:~/devel$ sudo snap install powershell
ошибка: This revision of snap "powershell" was published using classic confinement and thus
may perform arbitrary system changes outside of the security sandbox that snaps are
usually confined to, which may put your system at risk.

              If you understand and want to proceed repeat the command including --classic.
db@gb-linux:~/devel$ sudo snap install powershell --classic
powershell 7.3.2 от Microsoft PowerShell✓ установлен
db@gb-linux:~/devel$ sudo snap remove powershell
powershell удалён
db@gb-linux:~/devel$

# 8)   Добавить произвольную задачу для выполнения каждые 3 минуты (Например, запись в текстовый файл чего-то или копирование из каталога А в каталог Б).

db@gb-linux:~/devel$ nano script.sh
db@gb-linux:~/devel$ touch testcron.log
db@gb-linux:~/devel$ ls
script.sh  testcron.log  Игрушки
db@gb-linux:~/devel$ tail script.sh
#!/bin/bash
echo $(date) >> /home/dbgb/devel/testcron.log
db@gb-linux:~/devel$ ll

drwxrwxr-x  3 dbgb dbgb 4096 лют ./
drwxr-x--- 23 dbgb dbgb 4096 лют ../
-rw-rw-r--  1 dbgb dbgb   61 лют script.sh
-rw-rw-r--  1 dbgb dbgb    0 лют testcron.log
drwxrwxr-x  4 dbgb dbgb 4096 лют Игрушки/
db@gb-linux:~/devel$ sudo chmod ugo+x /home/dbgb/devel/script.sh
[sudo] пароль для db:
db@gb-linux:~/devel$ ll

drwxrwxr-x  3 dbgb dbgb 4096 лют ./
drwxr-x--- 23 dbgb dbgb 4096 лют ../
-rwxrwxr-x  1 dbgb dbgb   61 лют script.sh*
-rw-rw-r--  1 dbgb dbgb    0 лют testcron.log
drwxrwxr-x  4 dbgb dbgb 4096 лют Игрушки/
db@gb-linux:~/devel$ crontab -e
crontab: installing new crontab
db@gb-linux:~/devel$ sudo cat /var/log/syslog | grep CRON
db-linux CRON[40210]: (root) CMD (  [ -x /usr/lib/php/sessionclean ] && if [ ! -d /run/systemd/system ]; then /usr/lib/php/sessionclean; fi)
db-linux CRON[40299]: (root) CMD (   cd / && run-parts --report /etc/cron.hourly)
db-linux CRON[40307]: (root) CMD ([ -x /etc/init.d/anacron ] && if [ ! -d /run/systemd/system ]; then /usr/sbin/invoke-rc.d anacron start >/dev/null; fi)
db-linux cron[755]: (CRON) INFO (pidfile fd = 3)
db-linux cron[755]: (CRON) INFO (Running @reboot jobs)
db-linux CRON[2198]: (root) CMD (  [ -x /usr/lib/php/sessionclean ] && if [ ! -d /run/systemd/system ]; then /usr/lib/php/sessionclean; fi)
db-linux CRON[4469]: (root) CMD (  [ -x /usr/lib/php/sessionclean ] && if [ ! -d /run/systemd/system ]; then /usr/lib/php/sessionclean; fi)
db-linux CRON[4539]: (root) CMD (   cd / && run-parts --report /etc/cron.hourly)
db-linux CRON[4546]: (root) CMD ([ -x /etc/init.d/anacron ] && if [ ! -d /run/systemd/system ]; then /usr/sbin/invoke-rc.d anacron start >/dev/null; fi)
db-linux CRON[4612]: (root) CMD (  [ -x /usr/lib/php/sessionclean ] && if [ ! -d /run/systemd/system ]; then /usr/lib/php/sessionclean; fi)
db-linux CRON[4762]: (root) CMD (  [ -x /usr/lib/php/sessionclean ] && if [ ! -d /run/systemd/system ]; then /usr/lib/php/sessionclean; fi)
db-linux CRON[5080]: (root) CMD (   cd / && run-parts --report /etc/cron.hourly)
db-linux CRON[5192]: (root) CMD ([ -x /etc/init.d/anacron ] && if [ ! -d /run/systemd/system ]; then /usr/sbin/invoke-rc.d anacron start >/dev/null; fi)
db-linux CRON[5272]: (db) CMD (/home/dbgb/devel/script.sh)
db@gb-linux:~/devel$ tail /home/dbgb/devel/testcron.log