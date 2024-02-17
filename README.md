## Задача
###### Скрипт на bash для подсчета количества слов и средней длины слова в файле. Этапы для написания рабочего скрипта:
---
1. Создаем файл script.sh 
```bash
touch script.sh
```
2. Переходим в него для изменения 
```bash
nano script.sh
```
---
3. Вставляем данный скрипт

```bash
#!/bin/bash

file_path="example.txt"
total_words=$(wc -w < $file_path)
total_characters=$(wc -m < $file_path)
average_word_length=$(echo "scale=2; $total_characters / $total_words" | bc)

echo "Количество слов в файле: $total_words"
echo "Средняя длина слова: $average_word_length"
```
---
4. Даем права для исполнения скрипта chmod 
```bash
chmod +x script.sh
```
5. Создаем файл example.txt и добавляем в него нужный текст (в моем случае я взял текст из РыбаТекст). Важно! Чтобы файл example.txt был в одно дериктории со скриптом
---
Текст который используется у меня

Предварительные выводы неутешительны: сложившаяся структура организации прекрасно подходит для реализации распределения внутренних резервов и ресурсов. Современные технологии достигли такого уровня, что понимание сути ресурсосберегающих технологий предоставляет широкие возможности для благоприятных перспектив.
___
6. Запускаем скрипт командой 
```bash
./script.sh 
```
После запуска скрипт выведет общее количество слов в тексте и среднюю длину слова
![Alt text](image-1.png)
