# Лабораторная работа по теме "Планировщик задач at"
## Требования
1. Машина с установленной системой Linux
2. Доступ к терминалу

## Введение
1. Установка
```
sudo apt install at
```
Если служба atd не запустилась автоматически, её надо включить и запустить
```
sudo systemctl start atd
sudo systemctl enable atd
```
2. Создание напоминания  
После команды at запишите время, в которое хотите получить напоминание, например
```
at 14:47
```
Команду нужно записать после сообщения ```at>```
```
at> echo "This is my first reminder!" > message.txt
```
Нажиме Ctrl+D чтобы завершить создание напоминания. Проверьте корректность выполнения команды. В файле message.txt должно быть записано сообщение.  
  
  3. Передача задания в команду
```
echo "This is my second reminder!" >> message.txt | at now
```
Проверьте результат работы в файле message.txt

## Задание

Напишите скрипт, который при запуске выводит что-нибудь (например, точную дату и время). С помощью команды at запланируйте выполнение скрипта 3 раза в разное время: через 2 минуты, через неделю, через год. В отчёт надо включить список запланированных задач и результат выполнения скрипта 1 раз.
  
## Источники
https://itshaman.ru/articles/2032/kak-planirovat-zadachi-s-pomoshchyu-komandy-at  
https://phoenixnap.com/kb/linux-at-command  
https://www.baeldung.com/linux/at-command
