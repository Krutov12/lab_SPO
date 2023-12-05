# lab_SPO
1) Замените только первое появление 5 на five для данного источника стандартного ввода.

echo 'They ate 5 apples and 5 mangoes' | sed 's/5/five/'

<img width="543" alt="image" src="https://github.com/Krutov12/lab_SPO/assets/77206997/8ac5a904-973c-46bc-9992-1234a53d22d6">

2) Замените все вхождения 5 на пять.

echo 'They ate 5 apples and 5 mangoes' | sed 's/5/five/g'

<img width="540" alt="image" src="https://github.com/Krutov12/lab_SPO/assets/77206997/5c29bc13-cf49-4570-984b-02f133da6216">

3) Замените все вхождения 0xA0 на 0x50 и 0xFF на 0x7F для данного входного файла.

sed -e 's/0xA0/0x50/g' -e 's/0xFF/0x7F/g' hex.txt

<img width="573" alt="image" src="https://github.com/Krutov12/lab_SPO/assets/77206997/8ad7c680-3b12-41cd-b76e-33f8d34109c1">

4) Команда замены ищет и заменяет последовательности символов. Если вам нужно сопоставить один или несколько символов с другим набором соответствующих символов, вы можете использовать команду y. Цитата из мануала:
y/src/dst/ Transliterate any characters in the pattern space which match any of the source-chars with the corresponding character in dest-chars.
y/src/dst/ Транслитерирует любые символы в пространстве шаблонов, которые соответствуют любому из исходных символов, соответствующим символу в dest-символах.
Используйте команду y, чтобы преобразовать данную входную строку, чтобы получить выходную строку, как показано ниже.
Input:
'goal new user sit eat dinner'
Output:
gOAl nEw UsEr sIt EAt dInnEr

echo 'goal new user sit eat dinner' | sed 'y/aeiou/AEIOU/'

<img width="609" alt="image" src="https://github.com/Krutov12/lab_SPO/assets/77206997/cb40e686-110d-46f3-9a9a-75744172518b">

5) Почему следующая команда выдает ошибку? Как ты это исправил?

<img width="599" alt="image" src="https://github.com/Krutov12/lab_SPO/assets/77206997/144c62fa-848f-40c3-a396-eb2dcb8f4966">

Ошибка из-за того, что длина слов не совпадает
