---
sidebar_position: 10
---
# Теорія
## Об'єкт
Щоб більше розуміти як працюють об'єкти у програмуванні, давайте
введемо приклад з реального життя: наприклад, у вас є домашній вихованець. Нехай
це буде кіт.
Розглянемо його як об'єкт. У нього є назва (тобто його ідентифікатор серед
інших вихованців), є якісь властивості (наприклад, його ім'я, вік та вага), є
функції (наприклад, нявкання або засинання), є події (наприклад, знову ж таки,
коли кіт нявкнув або заснув).
Давайте візуалізуємо нашого кота:
![Кіт](images/oop_cat_ua.excalidraw.svg)
### Властивості
Властивість, грубо кажучи, це те саме, що й змінна, тільки вона прив'язана до
об'єкту.

### Функції
Раніше ми розглядали, що таке функції. Єдине, що відрізняється у
даному випадку - це те, що нам потрібен об'єкт (його екземпляр) щоб її викликати.

Екземпляр? Так як об'єкт - це самостійна структура, об'єкт може
існувати в декількох варіантах (наприклад, у вас може бути більше одного
кота). Це називають екземплярами об'єкта (тобто кількома варіаціями об'єкта).

### Події
Припустимо, що нашому коту потрібен спокійний і тривалий сон.
І нам потрібно поводитися тихіше, коли наш кіт у режимі сну.
Для цього ми повинні встановити візуальний контакт та дочекатися моменту, коли
наш кіт засне.
У програмуванні термін спостереження називають «слухачем». Слухач
отримує деяку інформацію, яку у ООП називають «повідомленням».

**Слухач** - сутність (aka об'єкт) з однією або декількома функціями, що
описують наші «повідомлення».

**Подія** - це повідомлення з якогось фрагмента коду іншому фрагменту коду.

### Інкапсуляція
Як ми вже розглянули, об'єкти мають властивості та функції. Що ж нам робити,
коли потрібно змінити якісь властивості всередині об'єкта? Наприклад, уявіть, що ми ведемо інстаграм-профіль нашого кота і нам потрібно змінити там
його вік або щось інше. На виручку, до нас приходить інкапсуляція.
Що таке інкапсуляція? Інкапсуляція - це властивість об'єкта змінювати свій
вміст (тобто свої внутрішні характеристики).
Повертаючись до кота, щоб змінити його вік, ми умовно створюємо функцію
оновити вік, що змінює властивість зсередини.

### Спадкування (або що там за абстракціями)
Ускладнимо завдання: у нас є притулок з домашніми тваринами, і нам потрібно
надати уніфіковану інформацію про кожну тварину.
Якщо ви раніше створювали таблиці в тому ж Excel, ви, швидше за все, розумієте, як ви можете виділити параметри кожного вихованця.

Що ж таке спадкування? **Спадкування** - це властивість об'єкта набувати
риси *іншого об'єкта*.

Як же вирішуватимемо завдання? Давайте спочатку виділимо, які вихованці у нас
взагалі є:
- собаки
- коти
- папуги

Тепер нашим завданням є знайти загальні властивості даних об'єктів (вихованців)
щоб виділити їх у більш загальну сутність.
Перше, що швидше за все, спало на думку — це імена. У всіх домашніх
тварин є якісь імена. Відразу ж після цього, буде неважко додумати
деякі інші властивості: скільки їм років, їх опис (може, наприклад, це
що говорящий папуга або кіт) та інші їх атрибути (властивості).
![Наслідування](images/oop_inheritance1_ua.excalidraw.svg)
*Вихованець тут — загальна сутність.*

Тепер, коли ми маємо загальну абстрактну сутність (aka об'єкт), ми можемо
підігнати наших котів, папуг і собак під цю сутність.
Спадкування гарантує, що виділена абстракція (aka загальна сутність)
буде задана об'єктом, що її успадковує. З цього випливає, що якщо ми розмістимо
список наших вихованців на нашому сайті, ми не отримаємо того, що наприклад у папуг немає зазначеного віку та ін.

### Абстрагування
Беремо олімп щодо ускладнення наших завдань: нам потрібно надати ветеринарний
паспорт заінтересованим особам. Але, паспорти, у нас, умовно, перебувають у
відмінному від знаходження вихованців місці. В іншому відділі, наприклад.
Не всім потрібно бачити паспорт доти, доки вони не оберуть вихованця, наприклад, за їхньою породою.
З'являється завдання абстрагувати не потрібні, спочатку, властивості. Для цього
Існує поняття абстрагування.
Абстрагування - уявний процес відділення властивостей об'єктів до якогось
ідеального стану зручного для нас.
У нашому випадку ми відокремили зайву інформацію для першообивателя.

### Поліморфізм
Вкотре ускладнимо завдання з нашими котиками та папугами: раніше було
сказано, ми не тримаємо вет. паспорти поруч із папугою, а десь в іншому відділі.
І коли потребується паспорт, ми дістанемо його з нашого 'сховища' (іншого відділу). Для розв'язання цього завдання є різні способи, що об'єднані одним терміном – поліморфізм.

Давайте введемо новий умовний об'єкт «Сховище», де у нас зберігатимуться
паспорти наших вихованців. Додамо туди функцію «отримати Паспорт» з аргументом
(aka параметром) «Кіт» (наш об'єкт, де зберігається інформація про нашого коте). Ну і
продублюємо ці функції так само для «Папуга» та «Собака» (так само наші об'єкти).

Що ж це виходить? Є три функції з однаковим ім'ям (aka
ідентифікатором), що, за ідеєю, має бути заборонено мовою програмування
(Aka компілятором). Але не так. Поліморфізм вирішує цю проблему,
вводячи подібну можливість (насправді трохи складніше, але поки що
зупинимося у цьому).

У програмуванні це називають *перевантаженням функції*. Коли функції мають
однакові імена, але різний набір параметрів.