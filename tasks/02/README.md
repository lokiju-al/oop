# Лабораторная работа №2. Знакомство со стандартной библиотекой шаблонов языка C++ <a name="lw"></a>

- [Лабораторная работа №2. Знакомство со стандартной библиотекой шаблонов языка C++ ](#лабораторная-работа-2-знакомство-со-стандартной-библиотекой-шаблонов-языка-c-)
  - [Практические задания](#практические-задания)
    - [Важное замечание](#важное-замечание)
  - [Обязательные задания](#обязательные-задания)
    - [Задание 1. Основы работы с контейнером vector. 20 баллов ](#задание-1-основы-работы-с-контейнером-vector-20-баллов-)
    - [Задание 2 – работа с контейнером string ](#задание-2--работа-с-контейнером-string-)
      - [Вариант 1 – TrimBlanks – 20 баллов ](#вариант-1--trimblanks--20-баллов-)
      - [Вариант 2 – RemoveExtraSpaces – 30 баллов ](#вариант-2--removeextraspaces--30-баллов-)
      - [Вариант 3 – FindAndReplace – 40 баллов ](#вариант-3--findandreplace--40-баллов-)
      - [Вариант 4 – HTML Encode – 40 баллов ](#вариант-4--html-encode--40-баллов-)
      - [Вариант 5 – HTML Decode – 60 баллов ](#вариант-5--html-decode--60-баллов-)
    - [Задание 3 – работа с контейнером map ](#задание-3--работа-с-контейнером-map-)
      - [Вариант 1- Подсчет частоты встречаемости слов – 40 баллов ](#вариант-1--подсчет-частоты-встречаемости-слов--40-баллов-)
      - [Вариант 2 – мини-словарь – 90 баллов ](#вариант-2--мини-словарь--90-баллов-)
    - [Задание 4. Работа с контейнером set ](#задание-4-работа-с-контейнером-set-)
      - [Вариант 1 – Cross Sets - 30 баллов ](#вариант-1--cross-sets---30-баллов-)
      - [Вариант 2 – Спортшкола – 40 баллов ](#вариант-2--спортшкола--40-баллов-)
      - [Вариант 3 – Фильтр нецензурных слов – 60 баллов ](#вариант-3--фильтр-нецензурных-слов--60-баллов-)
      - [Вариант 4 – Генератор простых чисел – 100 баллов ](#вариант-4--генератор-простых-чисел--100-баллов-)
  - [Дополнительные задания](#дополнительные-задания)
    - [Задание 5. – регулярные выражения ](#задание-5--регулярные-выражения-)
      - [Вариант 1 – парсер URL-ов – 80 баллов ](#вариант-1--парсер-url-ов--80-баллов-)
    - [Задание 6 ](#задание-6-)
      - [Вариант 1 – Expand Template - 100 баллов ](#вариант-1--expand-template---100-баллов-)
    - [Задание 7 ](#задание-7-)
      - [Вариант 1 — разбор выражения — 100 баллов ](#вариант-1--разбор-выражения--100-баллов-)

## Практические задания

Для получения оценки «**удовлетворительно**» необходимо набрать **не менее 80 баллов**.

Для получения оценки «**хорошо**» необходимо набрать **не менее 300 баллов**.

Для получения оценки «**отлично**» необходимо набрать **не менее 500 баллов**.

**Внимание**, дополнительные задания принимаются только после успешной защиты обязательных заданий.

### Важное замечание

<span style="color:red">При выполнении заданий следует отдавать предпочтение использованию алгоритмов STL, нежели написанию «сырых» циклов.
Рекомендуется посмотреть доклад (англ.) C++ Seasoning c конференции Going Native 2013, доступный по ссылке:</span>

https://channel9.msdn.com/Events/GoingNative/2013/Cpp-Seasoning

## Обязательные задания

### Задание 1. Основы работы с контейнером vector. 20 баллов <a name="1"></a>

Ознакомьтесь с возможностями класса [vector](https://en.cppreference.com/w/cpp/container/vector) библиотеки STL, а также с основными [алгоритмами STL](https://en.cppreference.com/w/cpp/algorithm/transform).

Разработайте программу, выполняющую считывание массива чисел с плавающей запятой, разделяемых пробелами, из стандартного потока ввода в vector,
обрабатывающую его согласно заданию Вашего варианта и выводящую в стандартный поток полученный массив (разделенный пробелами).
В программе должны быть выделены функции, выполняющие считывание массива,
его обработку (функция обработки вектора значений должна изменять содержимое переданного массива) и вывод результата.

**Подсказка**: чтобы вывести числа с желаемой точностью, воспользуйтесь манипуляторами вывода в поток:
[std::setprecision](https://en.cppreference.com/w/cpp/io/manip/setprecision), и [std::fixed](https://en.cppreference.com/w/cpp/io/manip/fixed).

Пустой массив, переданный программе – допустимые входные данные. При его обработке пустой массив должен оставаться пустым.

<span style="color:red">Для тестирования разрабатываемых функций должны быть разработаны тесты,
проверяющие корректность их работы на некотором разумном наборе входных параметров.</span>

<table>
    <thead>
        <tr>
            <th>Вариант</th>
            <th>Выводимое значение</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <th>1</th>
            <th>Прибавить к каждому элементу массива среднее арифметическое его положительных элементов
                Подсказка: используйте алгоритм std::accumulate, чтобы найти сумму положительных элементов.</th>
        </tr>
        <tr>
            <th>2</th>
            <th>Каждый элемент массива должен быть умножен на минимальный элемент исходного массива
                Подсказка: используйте алгоритм std::min_element.</th>
        </tr>
        <tr>
            <th>3</th>
            <th>Разделить элементы массива на половину максимального элемента.
                Подсказка: используйте std::max_element</th>
        </tr>
        <tr>
            <th>4</th>
            <th>Умножить каждый отрицательный элемент массива на произведение максимального и минимального элементов исходного массива
                Подсказка: используйте std::minmax_element, чтобы найти минимальный и максимальный элементы массива</th>
        </tr>
        <tr>
            <th>5</th>
            <th>Умножить каждый элемент массива на максимальный элемент исходного массива и разделить на минимальный элемент исходного массива
                Подсказка: используйте std::minmax_element, чтобы найти минимальный и максимальный элементы</th>
        </tr>
        <tr>
            <th>6</th>
            <th>Прибавить к каждому элементу массива сумму трех минимальных элементов массива.
            Если массив содержит меньше трех элементов, надо прибавить сумму имеющихся.
                Подсказка: используйте std::partial_sort_copy, чтобы найти три минимальных элемента.</th>
        </tr>
        <tr>
            <th>7</th>
            <th>Элементы, стоящие на четных позициях массива умножить на 2, а из элементов, стоящих на нечетных позициях,
            вычесть сумму всех неотрицательных элементов.
                Подсказка: используйте std::accumulate, чтобы найти сумму неотрицательных элементов.</th>
        </tr>
            <th>8</th>
            <th>Вычесть из каждого элемента исходного массива значение его медианы.
                Подсказка: используйте алгоритм std::nth_element, чтобы найти медианный элемент массива.
                Учтите, что `nth_element` изменяет порядок элементов контейнера.</th>
        </tr>
    </tbody>
</table>

<span style="color:gray">**Бонус 10 баллов за сортировку элементов массива в порядке возрастания**</span>

Бонус начисляется за вывод элементов массива в порядке возрастания их значений.
При этом функция обработки вектора, разработанная в основной части задания, не должна выполнять сортировку элементов. <a name="1-b-1"></a>

### Задание 2 – работа с контейнером string <a name="2"></a>

Ознакомьтесь с возможностями класса [string](https://en.cppreference.com/w/cpp/string/basic_string) (точнее, шаблона basic_string) библиотеки STL и
выполните задание, соответствующее номеру Вашего варианта.

<span style="color:red">Для тестирования разрабатываемых функций должны быть разработаны тесты,
проверяющие корректность их работы на некотором разумном наборе входных параметров.</span>

#### Вариант 1 – TrimBlanks – 20 баллов <a name="2-1"></a>

Разработайте функцию

```c++
std::string TrimBlanks(std::string const& str)
```

выполняющую отрезание пробелов в начале и в конце строки str, и возвращающую результирующую строку.
Если строка состоит из одних пробелов, должна вернуться пустая строка.

Разработайте на ее основе программу, выполняющую отрезание пробелов в начале и конце **каждой строки**,
поступающей со стандартного потока ввода, и выводящую результат в стандартный поток вывода.

<span style="color:red">Внимание, реализация данной функции должна иметь сложность не более O(N).</span>

#### Вариант 2 – RemoveExtraSpaces – 30 баллов <a name="2-2"></a>

Разработайте функцию

```c++
std::string RemoveExtraSpaces(std::string const& arg)
```

удаляющую из строки, переданной в параметре arg, лишние пробелы.
Лишними считаются все пробелы в начале и конце строки, а также дополнительные пробелы между словами.

Разработайте с ее использованием программу, выполняющую удаление лишних пробелов из каждой строки входного потока символов и
вывод результирующих строк в выходной поток.

<span style="color:red">Внимание, реализация данной функции должна иметь сложность не более O(N)</span>

### Вариант 3 – FindAndReplace – 40 баллов <a name="2-3"></a>

Разработайте функцию

```c++
std::string FindAndReplace(std::string const& subject, std::string const& search, std::string  const& replace)
```

возвращающую результат замены всех вхождений подстроки **search** в строке **subject** на строку **replace**.
Если искомая строка пустая, замены строк производиться не должно.

Вычислительная сложность алгоритма, лежащего в основе FindAndReplace, должна линейно зависеть от длины строки Subject

Разработайте на ее основе программу, заменяющую все вхождения искомой строки в стандартном потоке ввода на строку-заменитель и выводящую результат в стандартный поток вывода.
Чтение и замена вхождений подстроки должны проводиться строка за строкой. Ввод продолжается до появления символа конца файла в стандартном потоке ввода.

Синтаксис командной строки:

```sh
replace.exe <search-string> <replace-string>
```

<span style="color:red">Внимание, реализация данной функции должна иметь сложность близкую к O(N+M+k*L),
где N - длина текста, M - длина искомой строки, L - длина строки-заменителя, а k - количество вхождений искомой строки в тексте.</span>

Подсказка: воспользуйтесь алгоритмом [std::search](https://en.cppreference.com/w/cpp/algorithm/search)

#### Вариант 4 – HTML Encode – 40 баллов <a name="2-4"></a>

Разработайте функцию

```c++
std::string HtmlEncode(std::string const& text)
```

выполняющую кодирование специальных символов строки text соответствующими сущностями HTML:

- `"` (двойная кавычка) заменяется на `&quot;`
- `'` (апостроф) заменяется на `&apos;`
- `<` (знак меньше) заменяется на `&lt;`
- `>` (знак больше) заменяется на `&gt;`
- `&` (амперсанд) заменяется на `&amp;`

Например, строка `Cat <says> "Meow". M&M’s` должна быть преобразована в строку
`Cat &lt;says&gt; &quot;Meow&quot;. M&amp;M&apos;s`

Разработайте на ее основе программу, выполняющую построчное html-кодирование текста, поступающего со стандартного потока ввода, и выводящую результат в стандартный поток вывода.

Символы &, полученные в процессе кодирования, не должны повторно кодироваться.

<span style="color:red">Внимание, реализация данной функции должна иметь сложность близкую к O(N)</span>

#### Вариант 5 – HTML Decode – 60 баллов <a name="2-5"></a>

Разработайте функцию

```c++
std::string HtmlDecode(std::string const& html)
```

выполняющую декодирование HTML-сущностей строки **html**, перечисленных в варианте 4, обратно в их символьное представление.

Разработайте на ее основе программу, выполняющую построчное декодирование html-сущностей текста, поступающего со стандартного потока ввода,
и выводящую результат в стандартный поток вывода.

<span style="color:red">Внимание, реализация данной функции должна иметь сложность близкую к O(N)</span>

### Задание 3 – работа с контейнером map <a name="3"></a>

Ознакомьтесь с возможностями контейнера [std::map](https://en.cppreference.com/w/cpp/container/map) библиотеки STL и выполните задание, соответствующее номеру Вашего варианта.

<span style="color:red">Для тестирования разрабатываемых функций должны быть разработаны тесты, проверяющие корректность их работы на некотором разумном наборе входных параметров.</span>

#### Вариант 1- Подсчет частоты встречаемости слов – 40 баллов <a name="3-1"></a>

Разработайте программу, выполняющую подсчет частоты встречаемости слов, поступающих со стандартного потока ввода и выводящую слова их частоты их встречаемости в стандартный поток вывода.

Под словом понимается последовательность из одного и более символов, не являющихся пробелами, табуляциями, символами конца строки.

Частота встречаемости слов должна выводиться после того, как входной поток данных закончится (eof).

Для подсчета частоты встречаемости символов используйте отображение **слово→частота встречаемости**.

<span style="color:gray">**Бонус 10 баллов за подсчет слов, записанных в case-insensitive формате**</span> <a name="3-1-b-1"></a>

**Дополнительно можно получить до 10 баллов**, если программа будет способна обнаруживать русские и английские слова, записанные в разном регистре символов,
т.е. считать слова **HeLLo** и **heLLO** одинаковыми.

### Вариант 2 – мини-словарь – 90 баллов <a name="3-2"></a>

Разработайте программу-словарь, осуществляющую перевод **слов и словосочетаний**, поступающих со стандартного потока ввода,
**с английского языка на русский** с использованием заданного файла словаря и выводящую результат перевода в стандартный поток вывода.

Если вводимое слово или словосочетание, отсутствует в словаре, программа должна попросить пользователя ввести перевод и запомнить его, в случае, если пользователь ввел непустую строку.

**Для выхода из диалога с программой** пользователь должен ввести строку, **состоящую из трех точек**.
Перед выходом программа спрашивает о необходимости сохранить изменения в файле словаря, в том случае, **если в словарь были добавлены фразы** во время текущей сессии работы с программой.

Имя файла словаря передается программе с помощью параметра командной строки.
Если файл словаря отсутствует, то программа должна считать его пустым и предложить сохранить словарь по окончании работы, если туда были добавлены фразы.

Пример диалога <span style="color:red">пользователя</span> с <span style="color:#4682B4">программой</span>:

```txt
>cat
кот, кошка
>ball
мяч
>meat
Неизвестное слово “meat”. Введите перевод или пустую строку для отказа.
>мясо
Слово “meat” сохранено в словаре как “мясо”.
>meat
мясо
>The Red Square
Неизвестное слово “The Red Square”. Введите перевод или пустую строку для отказа.
>Красная Площадь
Слово “The Red Square” сохранено в словаре как “Красная Площадь”.
>lkkvksmdv
Неизвестное слово “lkkvksmdv”. Введите перевод или пустую строку для отказа.
>
Слово “lkkvksmdv”проигнорировано.
>...
В словарь были внесены изменения. Введите Y или y для сохранения перед выходом.
>y
Изменения сохранены. До свидания.
```

<span style="color:gray">**Бонус 10 баллов за возможность распознавания слов, записанных в разном регистре**</span> <a name="3-2-b-1"></a>

<span style="color:red">Дополнительно можно получить до 10 баллов</span>, если программа будет способна осуществлять перевод английских слов,
вводимых пользователем в произвольном регистре символов. Например, слова **CaT**, при известном переводе для слова **cat**. Регистр перевода теряться не должен.

<span style="color:gray">**Бонус 20 баллов за реализацию двунаправленного перевода**</span> <a name="3-2-b-2"></a>

<span style="color:red">Дополнительно можно получить до 20 баллов</span>, если программа сможет осуществлять и обратный перевод словосочетаний.
При этом необходимо поддержать возможность существования **нескольких вариантов** перевода одного и того же слова.

Например, после добавления слов «кошка»→«cat» и «кот»→«cat», программа должна иметь возможность перевести слово cat, выдав 2 возможных перевода.

### Задание 4. Работа с контейнером set <a name="4"></a>

Ознакомьтесь с возможностями контейнера [std::set](https://en.cppreference.com/w/cpp/container/set) и выполните задание, соответствующее номеру Вашего варианта.

<span style="color:red">Для тестирования разрабатываемых функций должны быть разработаны тесты, проверяющие корректность их работы на некотором разумном наборе входных параметров.</span>

#### Вариант 1 – Cross Sets - 30 баллов <a name="4-1"></a>

Разработайте функцию

```c++
std::set<int> CrossSet(std::set<int> const& set1, std::set<int> const& set2);
```

возвращающую результат пересечения (пересечением двух множеств является множество, содержащее элементы,
присутствующие одновременно и в первом и во втором множестве) двух множеств целых чисел.

С ее использованием разработайте программу, выводящую в стандартный поток вывода элементы двух множеств целых чисел и результат их пересечения.

**Первое множество** – множество чисел от 1 до N, делящихся без остатка на сумму своих цифр.

**Второе множество** – множество целых чисел то 1 до N, сумма цифр которых является четной.

Параметр N передается пользователем в виде аргумента командной строки.

**Подсказка**: используйте алгоритм **set_intersection**.

#### Вариант 2 – Спортшкола – 40 баллов <a name="4-2"></a>

В спортивной школе обучается некоторое количество учеников. Имена учеников – уникальны. Каждый ученик посещает одну или более спортивных секций школы.

У тренера каждой секции есть список учеников его секции, заданный в виде текстового файла, в котором в каждой строке записано ФИО ученика.

***Задача***: на основе файлов со списками учеников каждого тренера построить список всех учеников школы.

Программа принимает в качестве параметров командной строки имена файлов со списками учеников каждой секции (количество секций в школе, а,
следовательно, параметров командной строки – произвольно) и выводит в output список всех учащихся школы.

#### Вариант 3 – Фильтр нецензурных слов – 60 баллов <a name="4-3"></a>

Для повышения культуры общения в чате необходимо написать программу-фильтр, удаляющую из сообщений участников чата недопустимые слова.

Список недопустимых слов задается в текстовом файле (слова разделены последовательностью из одного и более пробелов, табуляций или символов конца строки),
имя которого передается программе при помощи аргумента командной строки.

Программа из каждой вводимой из стандартного потока ввода строки должна удалять присутствующие в ней недопустимые слова и выводить обработанный результат в стандартный поток ввода.

Под словом понимается последовательность из одного и более символов, разделенных последовательностью из одного и более символов-разделителей 
(пробелы, табуляции, символы конца строки, знаки препинания, знаки арифметических операций, скобки).

**Указания**: считайте недопустимые слова во множество строк и при обработке текста проверяйте вхождение каждого слова текста в данное множество.

<span style="color:gray">**Бонус в 10 баллов за распознавание нецензурных слов, записанных в разном регистре**</span> <a name="4-3-b-1"></a>

<span style="color:red">Дополнительно можно получить 10 баллов</span>, если фильтрация слов будет производиться с **игнорированием регистра символов**, в котором они записаны.
Т.е. если недопустимым словом является слово «дурак», то должны фильтроваться слова «ДуРак», «дурак», «ДУРАК» и подобные.

#### Вариант 4 – Генератор простых чисел – 100 баллов <a name="4-4"></a>

Разработайте функцию 

```c++
std::set<int> GeneratePrimeNumbersSet(int upperBound)
```

возвращающую множество всех простых чисел, **не превышающих** значения upperBound.

С ее использованием разработайте программу, выводящую в стандартный поток вывода элементы множества простых чисел,
не превышающие значения, переданного приложению через обязательный параметр командной строки.

Максимальное значение верхней границы множества принять равным 100 миллионам.

Время построения множества простых чисел в указанном диапазоне на компьютере с 2GHz-процессором не должно превышать 10-12 секунд (программа будет запускаться в Release-конфигурации).

Примечание: наивный поиск простых чисел не позволит добиться указанной производительности. Используйте «Решето Эратосфена».
Для предварительного просеивания воспользуйтесь `vector<bool>` (для хранения каждого элемента он использует 1 бит информации,
т.к. на хранение признака простоты 100 миллионов чисел потребуется всего 12,5 мегабайт памяти)

Для проверки программы используйте тот факт, что в диапазоне от 1 до 100000000 содержится 5761455 простых чисел.

## Дополнительные задания

### Задание 5. – регулярные выражения <a name="5"></a>

Ознакомьтесь с возможностями класса [std::regex](https://cplusplus.com/reference/regex/) и функций для работы с регулярными выражениями библиотеки STL и выполните задание, соответствующее номеру Вашего варианта.

<span style="color:red">Для тестирования разрабатываемых функций должны быть разработаны тесты, проверяющие корректность их работы на некотором разумном наборе входных параметров.</span>

#### Вариант 1 – парсер URL-ов – 80 баллов <a name="5-1"></a>

Разработайте функцию

```c++
bool ParseURL(string const& url, Protocol &  protocol, int & port, string & host, string & document)
```

выполняющую разбор строки url, и извлечение из нее информации об используемом протоколе, номере порта, имени хоста и имени документа.

В случае успеха функция должна возвращать true, в случае ошибки – false.

Protocol – это перечислимый тип, задающий один из известных программе протоколов:

```c++
enum class Protocol
{
    HTTP,
    HTTPS,
    FTP
};
```

Валидным (допустимым) URL-ом программа должна считать строку в следующем формате:

`протокол://хост[:порт][/документ]`, 

где протокол – http, https или ftp (**в любом регистре**),

порт – положительное число от 1 до 65535

хост – **непустая строка**

(в квадратных скобках указаны опциональные элементы URL-а)

Если порт не указан, то он должен считаться равным номеру порта по умолчанию для данного протокола (для HTTP – это 80, для HTTPS – 443, для FTP – 21).

Разработайте на ее основе программу, распознающую допустимые URL-строки в каждой вводимой пользователем строке ввода и выводящую в стандартный поток вывода информацию о **каждом URL-е** в следующем формате:

```sh
<Исходный URL>
HOST: <хост>
PORT: <порт>
DOC: <документ>
```

Например, для URL-а

`http://www.mysite.com/docs/document1.html?page=30&lang=en#title`

должно быть выведено:

```sh
http://www.mysite.com/docs/document1.html?page=30&lang=en#title
HOST: www.mysite.com
PORT: 80
DOC: docs/document1.html?page=30&lang=en#title
```

### Задание 6 <a name="6"></a>

#### Вариант 1 – Expand Template - 100 баллов <a name="6-1"></a>

Разработайте функцию

```c++
std::string ExpandTemplate(std::string const& tpl, std::map<std::string, std::string> const& params)
```

возвращающую результат подстановки параметров, заданных при помощи аргумента params (шаблонный параметр=>значение) в строку tpl. Пустые строки, выступающие в роли ключа в params, должны игнорироваться. Любой шаблонный параметр может встречаться в строке tpl произвольное количество раз. При наличии нескольких возможных вариантов подстановки должен выбираться параметр, имеющий наибольшую длину. Та часть строки tpl, в которую уже была выполнена подстановка, не должна повторно модифицироваться.

<span style="color:red">Для тестирования функции ExpandTemplate должны быть разработаны тесты, проверяющие корректность их работы на некотором разумном наборе входных параметров.</span>

Пример использования данной функции и ожидаемые результаты ее работы (приведенный пример проверяет лишь некоторые наиболее сложные из возможных ситуаций. Вместо обычных макросов assert следует использовать один из популярных C++-фреймворков для написания тестов):

```c++
using namespace std;

int main()
{
    {
        string const tpl = "Hello, %USER_NAME%. Today is {WEEK_DAY}.";
        map<string, string> params;
        params["%USER_NAME%"] = "Ivan Petrov";
        params["{WEEK_DAY}"] = "Friday";
        assert(ExpandTemplate(tpl, params) == "Hello, Ivan Petrov. Today is Friday.");
    }

    {
        string const tpl = "Hello, %USER_NAME%. Today is {WEEK_DAY}.";
        map<string, string> params;
        params["%USER_NAME%"] = "Super %USER_NAME% {WEEK_DAY}";
        params["{WEEK_DAY}"] = "Friday. {WEEK_DAY}";
        assert(ExpandTemplate(tpl, params) == 
            "Hello, Super %USER_NAME% {WEEK_DAY}. Today is Friday. {WEEK_DAY}.");
    }

    {
        string const tpl = "-AABBCCCCCABC+";
        map<string, string> params;
        params["A"] = "[a]";
        params["AA"] = "[aa]";
        params["B"] = "[b]";
        params["BB"] = "[bb]";
        params["C"] = "[c]";
        params["CC"] = "[cc]";
        assert(ExpandTemplate(tpl, params) == 
            "-[aa][bb][cc][cc][c][a][b][c]+");
    }
}
```

С использованием данной функции **разработайте приложение expand_template**, позволяющее заменить вхождения определенных строк в одном файле на определяемые пользователем и записать результат в выходной файл. Синтаксис командной строки приложения:

```sh
expand_template.exe <input-file> <output-file> [<param> <value> [<param> <value> …]]
```

Пример использования:

```sh
expand_template.exe input.txt output.txt "тепло" "холодно" "соленый" "сладкий" "день" "ночь"
```

записывает в выходной файл результат замены всех вхождений подстроки «тепло» на «холодно», «соленый» на «сладкий», «день» на «ночь», найденных во входном файле.

<span style="color:gray">**Бонус в 150 баллов за эффективное решение данной задачи с использованием алгоритма «Ахо-Корасик»**</span> <a name="6-1-b-1"></a>

Рекомендации по выполнению: для эффективной реализации данного задачи ознакомьтесь с алгоритмом «Ахо-Корасик» ([Википедия](https://ru.wikipedia.org/wiki/Алгоритм_Ахо_—_Корасик), [Хабрахабр](https://habr.com/ru/articles/198682/))

### Задание 7 <a name="7"></a>

#### Вариант 1 — разбор выражения — 100 баллов <a name="7-1"></a>

Программе в каждой строке стандартного ввода поступает арифметическое выражение в небинарной скобочной [польской нотации](https://ru.wikipedia.org/wiki/Польская_запись).

Программа должна вывести результат каждого из этих выражений выражения в виде числа.

Выражение в небинарной скобочной польской нотации имеет вид:

- (операция аргумент1 … аргументN)
- Операция имеет не менее одного аргумента
- Операция: либо сложение (символ +), либо умножение (символ *).
- Каждый аргумент – либо целое (положительное либо отрицательное) число, либо выражение в скобочной польской нотации.

Результат выражения – операция, применяемая ко всем аргументам.

Примеры ввода-вывода:

<table>
    <thead>
        <tr>
            <th>Ввод</th>
            <th>Вывод</th>
            <th>Примечание</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <th>(+ 7)</th>
            <th>7</th>
            <th>Если всего один аргумент, то результат выражения – этот самый аргумент</th>
        </tr>
        <tr>
            <th>(* 8)</th>
            <th>8</th>
            <th>Аналогично и тут</th>
        </tr>
        <tr>
            <th>(+ 2 3)</th>
            <th>5</th>
            <th>2 + 3 = 5</th>
        </tr>
        <tr>
            <th>(+ 2 3 4)</th>
            <th>9</th>
            <th>2 + 3 + 4 = 9</th>
        </tr>
        <tr>
            <th>(* 2 4)</th>
            <th>8</th>
            <th>2 * 4 = 8</th>
        </tr>
        <tr>
            <th>(* 2 3 4)</th>
            <th>24</th>
            <th>2 * 3 * 4 = 24</th>
        </tr>
        <tr>
            <th>(+ (* 2 3) (* 3 4))</th>
            <th>18</th>
            <th>(2 * 3) + (3 * 4) = 18</th>
        </tr>
        <tr>
            <th>(* (+ 1 2) (+ 3 1))</th>
            <th>12</th>
            <th>(1 + 2) * (3 + 1) = 12</th>
        </tr>
        <tr>
            <th>(+ 5 (* 2 3 2) (+ 5 (+ 2 5) (* 2 2) ))</th>
            <th>33</th>
            <th>5 + (2 * 3 * 2) + (5 + (2 + 5) + (2 * 2)) = 5 + 12 + 16 = 33</th>
        </tr>
        <tr>
            <th>(+ -2 3)</th>
            <th>1</th>
            <th>-2 + 3 = 1</th>
        </tr>
    </tbody>
</table>

Гарантируется, что программе поступают на вход синтаксически верные выражения.

Для работы над ней вам может понадобиться:

1) Уметь считывать символы из стандартного ввода:

   ```c++
   char ch;
   std::cin >> ch;
    ```

   Прочитает в переменную из cin первый непробельный символ.

2) Возвращать последний считанный символ обратно в поток `cin`:

   ```c++
   std::cin.unget();
   ```

Если после чтения символа вы решили вернуть его обратно в поток `cin`, то вызовите у потока метод `unget`.

Например

```c++
char ch1, ch2;
std::cin >> ch1;
std::cin.unget(); // вернули считанный символ в поток cin
std::cin >> ch2;
// В ch2 будет лежать тот же символ, что и в ch
```

Справочная информация

Нотация называется **скобочной**, так как выражение обязательно заключено в круглые скобки.

Нотация называется **небинарной**, так как количество аргументов может быть отлично от двух.

Нотация называется **польской**, так как её изобрёл польский математик Ян Лукасевич.

<span style="color:red">В программе должна быть выделена функция, вычисляющая значение выражения, записанного в обратной скобочной нотации. Для этой функции должны быть разработаны модульные тесты.</span>

<span style="color:gray">**Бонус в 50 баллов за обработку ошибок**</span> <a name="7-1-b-1"></a>

Если в строке содержится невалидное выражение, программа должна вывести строку **`ERROR`** вместо результата вычисления выражения. Вы можете использовать для обработки ошибок коды возврата из функции, либо механизм исключений.

<span style="color:gray">**Бонус в 80 баллов за нерекурсивное решение задачи**</span> <a name="7-1-b-2"></a>

Бонус начисляется, если для разбора выражения не используется рекурсия.
