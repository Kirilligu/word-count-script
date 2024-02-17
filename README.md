# word-count-script
Скрипт на bash для подсчета количества слов и средней длины слова в файле.
Этапы для написания рабочего скрипта:
1. Создаем файл sh
   touch script.sh

2. Переходим в него для изменения
   nano script.sh

3. Вставляем данный скрипт
   
#!/bin/bash

file_path="example.txt"
total_words=$(wc -w < $file_path)
total_characters=$(wc -m < $file_path)
average_word_length=$(echo "scale=2; $total_characters / $total_words" | bc)

echo "Количество слов в файле: $total_words"
echo "Средняя длина слова: $average_word_length"

Данный скрипт подсчитывает количество слов в файле example.txt, а также среднюю длину слов

4. Даем права для исполнения скрипта
   chmod +x word_count.sh

5. Создаем файл exampe.txt и добавляем в него нужный текст (в моем случае я взял текст из РыбаТекст). Важно! Чтобы файл example.txt был в одно дериктории со скриптом

6. Запускаем скрипт командой
   ./script.sh
   После запуска скрипт выведет общее количество слов в тексте и среднюю длину слова

   

