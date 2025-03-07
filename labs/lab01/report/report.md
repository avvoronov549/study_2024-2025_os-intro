---
## Front matter
title: "Лабораторная работа №1"
subtitle: "Дисциплина: Операционные системы"
author: "Воронов Александр Валерьевич"

## Generic otions
lang: ru-RU
toc-title: "Содержание"

## Bibliography
bibliography: bib/cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

## Pdf output format
toc: true # Table of contents
toc-depth: 2
lof: true # List of figures
lot: true # List of tables
fontsize: 12pt
linestretch: 1.5
papersize: a4
documentclass: scrreprt
## I18n polyglossia
polyglossia-lang:
  name: russian
  options:
	- spelling=modern
	- babelshorthands=true
polyglossia-otherlangs:
  name: english
## I18n babel
babel-lang: russian
babel-otherlangs: english
## Fonts
mainfont: IBM Plex Serif
romanfont: IBM Plex Serif
sansfont: IBM Plex Sans
monofont: IBM Plex Mono
mathfont: STIX Two Math
mainfontoptions: Ligatures=Common,Ligatures=TeX,Scale=0.94
romanfontoptions: Ligatures=Common,Ligatures=TeX,Scale=0.94
sansfontoptions: Ligatures=Common,Ligatures=TeX,Scale=MatchLowercase,Scale=0.94
monofontoptions: Scale=MatchLowercase,Scale=0.94,FakeStretch=0.9
mathfontoptions:
## Biblatex
biblatex: true
biblio-style: "gost-numeric"
biblatexoptions:
  - parentracker=true
  - backend=biber
  - hyperref=auto
  - language=auto
  - autolang=other*
  - citestyle=gost-numeric
## Pandoc-crossref LaTeX customization
figureTitle: "Рис."
tableTitle: "Таблица"
listingTitle: "Листинг"
lofTitle: "Список иллюстраций"
lotTitle: "Список таблиц"
lolTitle: "Листинги"
## Misc options
indent: true
header-includes:
  - \usepackage{indentfirst}
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Целью данной работы является приобретение практических навыков установки операционной системы на виртуальную машину, настройки минимально необходимых для дальнейшей работы сервисов.

# Задание

1. Запуск VirtualBox и создание новой виртуальной машины (операционная система Linux, Fedora)
2. Настройка установки ОС
3. Перезапуск виртуальной машины и установка драйверов для VirtualBox.
4. Подключение образа диска дополнений гостевой ОС.
5. Установка необходимого ПО для создания документации.
6. Выполнение домашнего задания.

# Теоретическое введение

Операционная система - это комплекс взаимосвязанных программ, который действует как интерфейс между приложениями и пользователями с одной стороны и аппаратурой компьютера с другой стороны. VirtualBox - это специальное средство для виртуализации, позволяющее запускать операционную систему внутри другой. С помощью VirtualBox мы можем также настраивать сеть, обмениваться файлами и делать многое другое 

# Выполнение лабораторной работы

## Создание виртуальной машины 
 
Создадим новую виртуальную машину, указав имя, размер основной памяти, размер видеопамяти, размер диска и других параметров на свое усмотрение, выбиарем образ системы Fedora (рис. [-@fig:001]).

![Настройки новой виртуальной машины](image/1.png){#fig:001 width=70%}

Начнем установку операционной системы, внеся перед этим необходимые для этого данные (рис. [-@fig:002]).

![Установка ОС](image/2.png){#fig:002 width=70%}

## После установки 

Войдем в ОС под своей учетной записью. В терминале через роль супер-пользователя устанавливаем средства разработки (рис. [-@fig:003]).

![Установка средств разработки](image/3.png){#fig:003 width=70%}

Обновляем пакеты все пакеты (рис. [-@fig:004]).

![Настройки новой виртуальной машины](image/4.png){#fig:004 width=70%}

Для повышения комфорта устанавливаем необходимые пакеты для удобства в консоли (рис. [-@fig:005]).

![Установка пакета для работы в консоли](image/5.png){#fig:005 width=70%}

Отключаем SELinux (рис. [-@fig:006]).

![Отключение SELinux](image/6.png){#fig:006 width=70%}

Устанавливаем менеджеров пакетов (рис. [-@fig:007]).

![Установка менеджера пакетов](image/7.png){#fig:007 width=70%}

Устанавливаем дистрибутив TexLive (рис. [-@fig:008]).

![Установка TexLive](image/8.png){#fig:008 width=70%}


## Выполнение домашнего задания 

Получаем информацию о версии ядра Linux, частоте процессора, модели процессора, объеме доступной оперативной памяти, типе обнаруженного гипервизора, типе файловой системе корневого раздела (рис. [-@fig:009]).

![Информация о системе](image/9.png){#fig:009 width=70%}

Продолжение (рис. [-@fig:010]).

![Информация о системе](image/10.png){#fig:010 width=70%}

# Контрольные вопросы

1) Какую информацию содержит учетная запись пользователя?
Имя пользователя, зашифрованный пароль пользователя, индентификационный номер пользователя, индентификационный номер группы пользователя, домашний каталог пользователя, командный интерпретатор пользователя.
                                                                                                          
2) Укажите команды терминала и приведите примеры: -для получения справки по команде: man man cd -ддя перемещения по файловой системе: cd cd ~/Downloads - для просмотра содержимого каталога: ls ls ~ Downloads - дл
я определения объема каталога: du du Downloads -для создания каталогов: mkdir mkdir ~ Downloads/New - для создания файлов: touch touch retouch - для удаления каталогов: rm rm dir1 - для удаления файлов: rm -r rm -r text.txt - для задания определенных прав на файл или каталог: chmod + x chmod +x text.txt -для просмотра истории команд: history
                                                                                                          
3) Что такое файловая система? Приведите примеры с краткой характеристикой.
Файловая система - это часть операционной системы, назначение которой состоит в том, чтобы обеспечить пользователю удобный интерфейс при работе с данными, хранящимися на диске, и обеспечить совместное использование файлов несколькими пользователями и процессорами. Примеры файловых систем: Ext2, Ext3, Ext4 или Extended Felisystem - стандартная файловая система для Linux. NTFS (New Technology File System): Стандартная файловая система для Windows.
                                                                                                          
4) Как посмотреть, какие файловые системы подмонтированы в ОС?
Команда mount
                                                                                                          
5) Как удалить зависший процесс?
Команда kill

# Выводы

В результате выполнения лабораторной работы я приобрел навыки установки операционной системы на виртуальную машину, а также настройки минимально необходимых для дальнейшей работы сервисов.

# Список литературы{.unnumbered}

