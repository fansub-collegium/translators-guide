# Гайд по использованию программы Aegisub для переводчиков.

## Предисловие

Aegisub — это программа для редактирования субтитров, ориентированная своим функционалом прежде всего на фансабберов.
Существуют два популярных формата субтитров — \*.srt и \*.ass. Первые просты по структуре, но позволяют только отображать текст без форматирования. Вторые позволяют делать сложное форматирование, применять эффекты, анимации. В фансабе используется в основном только \*.ass.

## Установка

Скачиваем программу [здесь](http://www.aegisub.org/downloads/).
Процесс установки не отличается от любой другой программы.
Сразу после установки рекомендую сделать две вещи:
1. Переключить язык на английский `Вид (View) -> Язык (Language)`. Перевод на русский кривоват, к тому же скриншоты будут использоваться с английской версии.
2. Поставить русский словарь для проверки орфографии. Крайне полезно после перевода пробежаться ещё раз спел-чекером по сабу. Дело в том, что изначально стоит только английский словарь, который проверяет английскую орфографию и подчёркивает все неверное (в том числе русские слова) красной волнистой линиией. С русским словарём он будет подчёркивать только то, что нам нужно. Качать [здесь](http://ftp.aegisub.org/pub/releases/dictionaries/Aegisub-3.0-dict-ru_RU.exe). Устанавливать в ту же папку, что и аегу. Будет предупреждение, что папка уже существует, нужно просто нажать "Далее". Свидетельством успешной установки будет то, что в папке с программой в папке dictionaries появятся файлы с RU в названии. Как им пользоваться, будет рассказано ниже.

## Процесс перевода

### Получаем видео

В начале нужно скачать серию. Обычно это делается через протокол BitTorrent с сайтов [nyaa.si](https://nyaa.si/) (без VPN не работает), [erai-raws.info](https://erai-raws.info/) (можно качать напрямую, без торрента), [horriblesubs.info](https://horriblesubs.info/) (можно качать через IRQ бота, на сайте есть гайд). Стабильнее всего хорриблы, у эраев много субтитров в комплекте, а няшка - по сути большой агрегатор, куда стягивается весь анимешный контент интернета. Для понимания — на всех этих сайтах ворованный контент с лицензионных стриминговых сервисов, вроде Crunchyroll, Funimation, Amazon Prime и других.

### Краткий экскурс по программе

![basic-interface](https://github.com/suisei-v/translators-guide/blob/master/images/basic-interface.png)

1. Окно со всеми субтитрами в открытом файле. При нажатии на строке выделяет её и позволяет редактировать в поле 3.
2. Кнопки слева направо: Старт видео, Проиграть видео для текущего саба, Пауза, Вкл/выкл поведение, когда при выделении саба видео перематывается на его начало.
3. Поле для редактирования саба.
4. Чекбокс `Show Original` — разделяет поле для редактирования на 2 половины, показывая в верхней части состояние до редактирования. Очень удобно при переводе.
5. Кнопка редактирования стиля для текущего саба. Там можно поменять цвет, размер, шрифт, выравнивание и многое другое для стиля. Стиль - это набор параметров форматирования, который можно применить сразу ко многим сабам. Функционал полезен при оформлении, но и переводчику может пригодится, если например слишком мелкий шрифт.
6. Правый ползунок — регулятор громкости.

### Переводим

Открываем программу. Нажимаем `Video -> Open Video`, открываем нужный видео-файл. Ну или просто перетаскиваем файл в окно аеги.
Далее нажимаем `File -> Open Subtitles from Video`. Если спросят, нужно ли сохранить файл Untitled, отвечаем, что нет. Далее следуем простому алгоритму:

1. Выбираем строчку для перевода.
2. Переводим.
3. Повторить пункты 1-2, пока перевод не будет завершён.

> Если после пункта 1 нажать Enter, то можно сразу перейти к следующему сабу.

Как вариант, можно использовать `Subtitle -> Translation Assistance`. Как им пользоваться, описано [здесь](http://docs.aegisub.org/3.2/Translation_Assistant/).

### Дополнительные требования

#### Ударения

Во всех именах, терминах, названиях нужно проставлять ударения. Крайне рекомендуется завести словарь и обновлять его с каждой серией. Ударения во всех сериях должны совпадать. 

Чтобы поставить ударение, нужно скопировать символ ударе́ния ( ́ ) и вста́вить его по́сле необходи́мой гла́сной. **Важно! Нельзя использовать французские и другие подобные символы со встроенными диактрическими знаками! Используйте только символ ударения, юникод U+0301.**

#### CPS

У каждого саба есть численный показать CPS (character per second). Характеризует, как быстро человек вынужден читать/говорить текст. Обычно значение варьируется в районе 10 с обычной речью, до 15 с быстрой и около 7-8 с медленной. При переводе этот параметр должен соблюдаться, и цифра не должна становиться красной. Но главный критерий — чтобы сказанная фраза на русском длилась ровно столько же, сколько и на японском, желательно с соблюдением пауз. Поэтому каждую фразу нужно проговаривать.

#### Надписи

Любые надписи, буде они встретятся, необходимо выделить в сабе меткой "Sign" в графе `Effect`:

![sign-in-effect](https://github.com/suisei-v/translators-guide/blob/master/images/sign-in-effect.png)

Благодаря этому в окне со всеми сабами (поле 1) появится графа `Effect`, и оформитель сможет сразу увидеть, где находится надпись, и оформить её. 

![sign-in-effect2](https://github.com/suisei-v/translators-guide/blob/master/images/sign-in-effect2.png)

Если на экране есть надпись на английском (или японском, если есть возможность с него перевести), в сабе её может не быть. Эту надпись всё равно нужно перевести, вставив новую строчку в саб. Для этого мотаем видео на нужный кадр, нажимаем правой кнопкой по ближайшему к надписи сабу и выбираем `Insert at video time (before)` (или after).

> Нажмите Ctrl+Space чтобы сделать фокус на видео, и тогда стрелками вправо-влево можно листать видео по-кадрово.

#### Двойные сабы

Бывает такая ситуация, когда в одной строчке оригинального саба находятся 2 фразы разных персонажей.

![double-sub](https://github.com/suisei-v/translators-guide/blob/master/images/double-sub.jpg)

> \N в тексте саба служит для переноса строки. Чтобы вставить, надо нажать Shift+Enter (или ввести вручную). Обычно, если в сабе 2 предложения, их лучше разделять этим символом для удобочитаемости.

Такой двойной саб необходимо разбивать на 2 отдельные строки. Рассмотрим два случая и алгоритм действий для каждого:

##### Персонажи говорят одновременно

1. Правой кнопкой мыши по сабу в гриде (поле 1) -> `Duplicate Lines`
2. В первом сабе убрать вторую реплику.
3. Во втором сабе убрать первую реплику.
4. Перед второстепенной репликой прописать тэг {\an8}. Это перенесет саб в верхнюю часть экрана. 

> an - сокращение от alignment, 8 - код выравнивания саба по нумпаду (8 - сверху, 4 - слева, 2 - стандартно снизу)

##### Персонажи говорят последовательно

1. Прослушать саб, запомнить место перехода с одной реплики на другую.
2. Прослушать второй раз, и в момент перехода нажать Ctrl+D.
3. В первом сабе убрать вторую реплику.
4. Во втором сабе убрать первую реплику.

## Как пользоваться словарём и спел-чекером

После перевода крайне рекомендуется пробежаться по сабу спел-чекером. Но перед этим, убедитесь что установлен русский словарь. После установки, щёлкаем правой кнопкой по полю редактирования, и выбираем новый словарь.

![change-dict](https://github.com/suisei-v/translators-guide/blob/master/images/change-dict.png)

После этого выделяем первую строчку саба и нажимаем `Subtitle -> Spell Checker`. Появится окно в котором мы нажимаем Ignore, чтобы пропустить текущую ошибку (например, имена и термины), и Replace, чтобы заменить на новый текст. Всё достаточно прозрачно, но более подробно интерфейс этой утилиты описан всё в том же [мануале](http://docs.aegisub.org/3.2/Spell_Checker/).

