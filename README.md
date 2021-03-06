# SP1
`Индивидуальная практическая работа №1`  
**`Вариант 5`**

Оконное приложение Win 32 
____
```
Указания по выбору варианта:  
Цель данной работы – практическое изучение построения и
функционирования типичных оконных приложений, элементов управления,
сообщений, средств графического вывода, используемых при этом основных
функций Win32 API, а также ознакомление со средой программирования. В
рамках заданий предполагается создание каркаса приложения, использование
сообщений, оконных объектов, взаимодействие с графической подсистемой,
реализованные на уровне системных вызовов Win 32 API.  

Индивидуальная практическая работа предполагает защиту выполненного
задания, а также ответы на теоретические вопросы, демонстрирующие владение
тематикой.  

Индивидуальная практическая работа оформляется в соответствии с
общеустановленными нормами и правилами.  

Выбор вариантов индивидуальной практической работы осуществляется
студентом самостоятельно на основании номера зачетной книжки (последние
цифры, после номера группы). Если порядковый номер превышает количество
вариантов, для выбора номера варианта используется остаток от деления
порядкового номера на количество вариантов. В отдельных случаях задание
может быть сформулировано преподавателем индивидуально.  
```
____
```
Теоретическая часть (вопросы):  
1. Стандартная структура оконного приложения, его основные функции.
2. Окно как системный объект. Функция создания нового окна и ее
параметры.
3. Оконный класс, виды оконных классов, создание оконного класса.
4. Пользовательские (настраиваеые) атрибуты окон.
5. Функции UpdateWindow() и ShowWindow().
6. Сообщение Windows (Win Message), его основные параметры. Очередь
сообщений. Способы отправки сообщений.
7. Цикл приема и обработки сообщений, функции GetMessage(),
TranslateMessage(), DispatchMessage(), завершение цикла.
8. Оконная процедура – назначение, структура, параметры, способы
вызова.
9. Перерисовка окна, последовательность формирования изображения,
сообщение WM_PAINT, функции GetWindowRect(), InvalidateRect().
10. Создание и использование элементов управления, меню. Сообщение
WM_COMMAND.
11. Таймеры. Создание, удаление, использование таймера (сообщение
WM_TIMER).
12. Элементов управления – виды, создание, использование. Элементы
управления Edit, Button, ListBox, ComboBox и т.д.
52
13. Обработка событий элемента управления (на примере элемента
Button).
14. Группировка элементов управления, доступ к группам, обработка
сообщений (на примере RadioButton, CheckBox).
15. Получение доступа к данным элемента управления (на примере текста
элемента Edit).
16. Элементы управления со сложными структурами данных (на примере
элементов ListBox, ComboBox и т.п.).
17. Контексты графических устройств.
18. Настройка графического контекста – система координат, единицы
измерения, управление цветом и т.д.
19. Объекты (инструменты) графической подсистемы. Порядок
применения инструментов для формирования изображения.
20. Активные инструменты Pen, Brush, Font, их создание и параметры.
21. Векторная графика, графические примитивы. Функции графических
примитивов, их параметры.
22. Средства растровой графики GDI.
23. Самоотрисовывающиеся (ownerdraw) элементы управления (на
примере кнопки) – формирование пользовательского изображения, обработка
событий.
24. Использование теневых графических контекстов. Анимация
изображений.
25. Сообщения как средство интерфейса между окнами. Использование
сообщений WM_USER.
26. Регистрация и использование пользовательских сообщений.
```
____
```
Вариант задания №5.
Программа с взаимодействующими элементами управления: окно
программы содержит два элемента ListBox, один Edit и четыре Button («Add»,
«Clear», «ToRight» и «Delete»). При нажатии на кнопку «Add» текст из Edit
должен добавляться в первый ListBox, если такого текста там еще нет
(необходимо выполнить проверку). Нажатие кнопки «Clear» очищает оба
ListBox-а. Нажатие кнопки «ToRight» копирует выделенную строку из первого
ListBox во второй (если там еще нет такой строки). Нажатие кнопки «Delete»
удаляет выделенные строки в каждом из ListBox-ов.
```
