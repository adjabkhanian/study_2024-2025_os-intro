---
## Front matter
title: "Отчет по выполнению лабораторной работы №8"
subtitle: "Анализ файловой системы Linux. Команды для работы с файлами"
author: "Аджабханян Овик"

## Generic options
lang: ru-RU
toc-title: "Содержание"

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
mainfont: Liberation Serif
romanfont: Liberation Serif
sansfont: Liberation Sans
monofont: Liberation Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase,Scale=0.9
## Misc options
indent: true
header-includes:
  - \usepackage{indentfirst}
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Цель данной лабораторной работы — изучить работу с файловой системой Linux, закрепить навыки использования команд `ls`, `grep`, `find`, `df`, `du`, управления процессами и работы с перенаправлением потоков ввода/вывода.

# Выполнение лабораторной работы

**1. Запись содержимого каталога /etc в файл file.txt**  

![Рис. 1 — запись списка файлов /etc в file.txt](image/01.png){#fig:001 width=70%}

**2. Дополнение файла названиями файлов из домашнего каталога и поиск .conf**  

![Рис. 2 — добавление файлов из домашнего каталога и фильтрация .conf](image/02.png){#fig:002 width=70%}

**3. Результат поиска файлов с расширением .conf**  

![Рис. 3 — найденные конфигурационные файлы](image/03.png){#fig:003 width=70%}

**4. Попытка записи логов в файл logfile в фоне**  

![Рис. 4 — запуск процесса для записи log* в logfile](image/04.png){#fig:004 width=70%}

**5. Определение файлов в домашнем каталоге, начинающихся с c**  

![Рис. 5 — поиск файлов, начинающихся с c](image/05.png){#fig:005 width=70%}

**6. Запуск редактора gedit в фоновом режиме**  

![Рис. 6 — запуск gedit в фоне](image/06.png){#fig:006 width=70%}

**7. Определение PID процесса gedit командой ps aux | grep**  

![Рис. 7 — поиск процесса gedit](image/07.png){#fig:007 width=70%}

**8. Завершение процесса gedit командой kill**  

![Рис. 8 — завершение процесса gedit](image/08.png){#fig:008 width=70%}

**9. Использование команды pgrep для поиска PID**  

![Рис. 9 — использование pgrep](image/09.png){#fig:009 width=70%}

**10. Удаление файла logfile**  

![Рис. 10 — удаление logfile](image/10.png){#fig:010 width=70%}

**11. Просмотр справки man для df и du**  

![Рис. 11 — man df](image/11.png){#fig:011 width=70%}  
![Рис. 12 — man du](image/12.png){#fig:012 width=70%}

**12. Просмотр информации о файловой системе df -h**  

![Рис. 13 — вывод df -h](image/13.png){#fig:013 width=70%}

**13. Просмотр размера домашнего каталога командой du -h ~**  

![Рис. 14 — вывод du -h ~](image/14.png){#fig:014 width=70%}

**14. Поиск всех директорий в домашнем каталоге командой find**  

![Рис. 15 — вывод find ~ -type d](image/15.png){#fig:015 width=70%}

# Выводы

В ходе выполнения лабораторной работы я научился:  
- использовать перенаправление потоков `>` и `>>`;  
- фильтровать файлы по маске и расширению через `grep`;  
- искать каталоги через `find`;  
- управлять процессами (`ps`, `pgrep`, `kill`);  
- анализировать файловую систему командами `df`, `du`.  

# Ответы на контрольные вопросы

1. **Потоки ввода/вывода:** стандартный ввод (stdin), стандартный вывод (stdout), стандартный вывод ошибок (stderr).  
2. **Разница между > и >>:** `>` перезаписывает файл, `>>` добавляет данные в конец.  
3. **Конвейер:** механизм передачи вывода одной команды на вход другой (`|`).  
4. **Процесс и программа:** программа — набор инструкций на диске, процесс — выполняющаяся программа в памяти.  
5. **PID и GID:** PID — идентификатор процесса, GID — идентификатор группы процессов.  
6. **Задачи:** это процессы в фоновом режиме, управляются командой `jobs`, `fg`, `bg`.  
7. **Утилиты top и htop:** отображают информацию о процессах и использовании ресурсов в реальном времени; `htop` удобнее благодаря интерфейсу и навигации.  
8. **Команда поиска файлов:** `find`, пример: `find ~ -name "*.txt"`.  
9. **Поиск по содержимому файла:** `grep "строка" файл` или `grep -r "строка" каталог`.  
10. **Определение объема свободной памяти на диске:** `df -h`.  
11. **Определение объема домашнего каталога:** `du -h ~`.  
12. **Удаление зависшего процесса:** `kill PID` или `kill -9 PID`.  

