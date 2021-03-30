# pp2
Week 4
regex . - Один любой символ, кроме новой строки 
\n. (h.l.o -> hello, hillo, halbo) 
\d - цифра (BD\d\d -> BD02, BD13) 
\D - Любой символ, кроме цифры (B\D\d. -> BA5l, BF25) 
\w - Любой символ (\w\w\w -> 123, a3b, a_!) 
\W Любая не-буква, не-цифра и не подчёркивание 
[..] - Один из символов в скобках, а также любой символ из диапазона a-b [0-9][0-9A-Fa-f] -> 12, 1F, 4B 
[^..] - Любой символ, кроме перечисленных 
\b - Начало или конец слова (слева пусто или не-буква, справа буква и наоборот). В отличие от предыдущих соответствует позиции, а не символу 
\bвал вал, перевал, Перевалка ^ Starts with $ Ends with 
{} Exactly the specified number of occurrences 
{n} Ровно n повторений 
(\d{4}) {m,n} От m до n повторений включительно 
(\d{2,4}) {m,} Не менее m повторений 
\d{3,} {,n} Не более n повторений ? Ноль или одно вхождение, синоним {0,1}

Ноль или более, синоним {0,}
Одно или более, синоним {1,}
| Either or () Capture and group \b Returns a match where the specified characters are at the beginning or at the end of a word (the "r" in the beginning is making sure that the string is being treated as a "raw string")

\d{5} - цифры ровно 5 раз \d\d/\d\d/\d{4} - дата в формате ДД/ММ/ГГГГ (но есть исключения) 
\d{2}:\d{2}:\d{2} - Selecting time with format: 14:56:10 
[-+]?\d+ -- число -1, 74, 00012 [-+]? — либо -, либо +, либо пусто 
\d+ — последовательность из 1 или более цифр [0-9]+ - все числа \w+stan Kazakhstan, Kyrgyzstan, Uzbekistan 
(+7|8)(?\d{3})?-?\d{3}-\d{2}-\d{2} - +7707-123-11-22 ----- +7(707)123-11-22 ---- 8(707)123-11-22 
[a-z]+@[a-z]+.[a-z]{2,5} - asd@gmail.com 
[a-z0-9_]+@[a-z]+.[a-z]{2,5} - asd3_asd@gmail.com 
[A-Za-z0-9_]+.?[A-Za-z0-9_]+@[a-z]+.[a-z]{2,4} - askar.akshabayev@gmail.com 
[\w]+.?[\w]+@[\w]+.[\w]{2,4} - askar.akshabayev@gmail.com