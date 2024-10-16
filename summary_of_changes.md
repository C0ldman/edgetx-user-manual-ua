---
опис: поточна версія для всіх об’єднаних Pull Requests станом на 31/05/2024 (v2.10.1)
---

# Опис змін із v2.9

Нижче наведено короткий перелік змін, які впливають на інтерфейс користувача та/або функціонування EdgeTX. Він не охоплює всі виправлення помилок. Щоб отримати повний список змін (включаючи виправлення помилок), прочитайте примітки до випуску.

### **Апаратури із кольоровим екраном**

* Підтримка нових апаратур
  * Flysky PL18
  * Flysky PL18 EV
  * Jumper T15
* Загальні зміни
  * Мікшер тепер працює на частоті 1000 Гц у режимі USB-джойстика (потрібен для учасників F.Sim), також відображає час роботи мікшера на екрані статистики/налагодження.
  * Незначні покращення інтерфейсу користувача на багатьох сторінках для кращого вигляду та узгодженості.
  * Видалено фон завантажувача, щоб зробити текст більш читабельним.
  * Стандартний екран завантаження оновлено новим логотипом EdgeTX і інформацією про версію EdgeTX.
  * Меню **Джерело** було оптимізовано для полегшення сенсорного використання та сортування.
  * Меню **Джерело** тепер відображатиме номер і назву глобальної змінної.
  * Додано світлодіодну анімацію зарядки для PL18 і PL18EV.
* [Сторінка інтерфейсу користувача](color-radios/user-interface/)
  * Кнопки **Система \[SYS]** і **Моделі \[MDL]** мають різні [функціональні можливості](color-radios/user-interface/#additional-system-and-model-button-functionalities) залежно від екрану, на якому вони використовуються.
  * [Перемикачі триммерів] (color-radios/user-interface/trim-navigation.md) на NV14 та EL18 тепер можна використовувати для навігації по меню.
  * Додано [апаратні клавіші швидкого доступу до віртуальної текстової та цифрової клавіатур](color-radios/user-interface/virtual-keyboards.md).
* [Керування моделями](color-radios/select-model.md)
  * Додано 3 додаткові макети для списку моделей.
  * Оновлено розмір і форму рамок зображень моделі. Також, тепер назва моделі відображається поверх зображення замість обрізання зображення.
  * Кнопки **Нова мітка** і **Нова модель** замінено просто кнопкою **Нова** з опціями **Модель** або **Мітка**.
  * Замінено заплутані піктограми сортування моделей простим текстовим спадним меню.
  * Додано єдиний параметр вибору для міток моделей, а також логіку фільтрації міток І/АБО (можна налаштувати на екрані [Налаштування радіо](color-radios/radio-settings/radio-setup/additional-radio-settings.md)).
* [Налаштування моделі](color-radios/model-settings/model-setup/)
  * Увімкнені таймери відображатимуться як виділені на екрані **Налаштування моделі**..
  * &#x20;MIN можна використовувати як джерело. Якщо вибрано, завжди повертатиметься -100.
  * До розділу **Передпольотні перевірки** додано **Інтерактивний** **Чекліст**. Дозволяє користувачам додавати інтерактивні чекбокси до відображених чеклістів.
* [Режими польоту](color-radios/model-settings/flight-modes.md)
  * Невикористані триммери тепер можна налаштувати як 3-позиційні миттєві перемикачі.
* [Мікшери](color-radios/model-settings/inputs-mixes-and-outputs/mixes.md)
  * Додано настроювану точність для **уповільнення** для встановлення 10 мс або 100 мс.
* [Глобальні змінні](color-radios/model-settings/global-variables.md)
  * Додано параметр **Спливаюче вікно**, який, коли ввімкнено, відображає спливаюче повідомлення, коли значення глобальної змінної змінюється новим.
* [Спеціальні функції](color-radios/model-settings/special-functions.md)
  * Усі спеціальні функції тепер мають прапорець **Увімкнути**.
  * Спеціальні функції можна ввімкнути/вимкнути, не відкриваючи меню редагування.
  * Додано перемикач віртуального тренера (**Tnr**), який можна вибрати як перемикач для активації спеціальної функції. Перемикач увімкнено, коли активне з'єднання тренера.
  * Значення спеціальної функції **Підсвітка** обмежені значеннями On/Off, налаштованими в **Налаштування апаратури -> Яскравість екрану.**
* [Телеметрія](color-radios/model-settings/telemetry/)
  * EdgeTX відтворить "Телеметрію підключено", коли телеметрія підключиться вперше під час польоту.
* [SD-карта](color-radios/radio-settings/sd-card.md)
  * Користувачі можуть налаштувати спеціальне зображення вимкнення, додавши спеціальний `shutdown.png` до папки **IMAGES**.
  * Параметр **Перегляд тексту** тепер доступний для файлів .lua
* [Налаштування апаратури](color-radios/radio-settings/radio-setup/)
  * У **Налаштуваннях GPS** оновлено параметр **Часовий пояс**, щоб дозволити налаштування з 15-хвилинними інтервалами.
  * Додано опцію **Заставка**, яка встановлює тривалість відображення заставки.
  * Додано опцію **Звук запуску**, яка вмикає чи вимикає звук запуску.
  * Додано параметр **Одиниці PPM** - раніше це був варіант збірки.
  * У розділі **Увімкнені функції** додано поточні параметри конфігурації для активної моделі праворуч від перемикача.
* [Апаратне забезпечення](color-radios/radio-settings/hardware.md)
  * Аналогові входи, такі як потенціометри та повзунки, тепер можна налаштувати як **Перемикач**, **Вісь X** або **Вісь Y**. Крім того, їх також можна налаштувати так, щоб вони були _**інвертовані**_.
  * EdgeTX тепер визначатиме під час виконання, чи доступний послідовний порт, щоб дозволити тренер SBUS у відсіку зовнішнього модуля. Якщо так, параметр конфігурації буде доступним.
* [Параметри екрана](color-radios/screen-settings/)
  * На верхній панелі інформація про апаратуру, дата/час і внутрішній GPS тепер є настроюваними віджетами, що дозволяє налаштувати 6 слотів для віджетів.
  * Якщо вибрати порожній віджет, опція «Вибрати віджет» більше не відображатиметься, а натомість перейде прямо до меню вибору віджета.
  [Віджети](color-radios/screen-settings/widgets.md)
  * Додано опцію вирівнювання для віджета **Текст**, щоб вирівняти текст віджета **Ліворуч**, **Центр** або **Праворуч**.
* Сповіщення
  * Попередження буде відображено, якщо ви спробуєте вимкнути апаратуру, коли підключення тренера все ще активне.

### Апаратури з монохромним екраном

* Підтримка нових апаратур
  * Jumper T-Pro V2
  * Jumper T-14
  * Jumper T-20
  * Flysky Gimbal підтримка для Jumper T-20
  * Flysky Gimbal підтримка для Frsky X9D+2019
  * RadioMaster Pocket
  * RadioMaster MT12
* Загальні зміни
  * Мікшер тепер працює на частоті 1000 Гц у режимі USB-джойстика (потрібен для учасників F.Sim), також відображає час роботи мікшера на екрані статистики/налагодження.
  * Екран завантаження оновлено новим логотипом EdgeTX.
  * Апаратури з невикористаним послідовним портом тепер автоматично визначатимуться як **AUX Serial** (MT12).
* [Головний екран](bw-radios/main-view/)
  * Додано новий екран для наземних апаратур із газом і рулевим колесом замість стіків.
* [Параметри моделі](bw-radios/model-select/)
  * Додано опцію **C-Interact** до розділу передпольотних перевірок. Дозволяє користувачам додавати інтерактивні чекбокси до відображених чеклістів.
  * На наземних апаратурах (наприклад: MT-12) триммер газу більше не впливає на діапазон заднього ходу газу.
* [Режими польоту](bw-radios/model-select/flight-modes.md)
  * Невикористані триммери тепер можна налаштувати як 3-позиційні перемикачі.
* [Мікшери](bw-radios/model-select/inputs-mixes-and-outputs/mixes.md)
  * Додано настроювану точність для **уповільнення** для встановлення 10 мс або 100 мс.
* [Телеметрія](bw-radios/model-select/telemetry/)
  * EdgeTX відтворить "Телеметрію підключено", коли телеметрія підключиться вперше під час польоту.
  * Кількість налаштованих датчиків відображатиметься в **дужках**, коли список датчиків згорнуто.
* [Спеціальні функції](bw-radios/model-select/special-functions.md)
  * Усі спеціальні функції тепер мають прапорець **Увімкнути**.
  * Яскравість OLED екрану можна контролювати за допомогою спеціальної функції **Підсвічування**.
  * Додано перемикач віртуального тренера (**Tnr**), який можна вибрати як перемикач для активації спеціальної функції. Перемикач увімкнено, коли активне з'єднання тренера.
  * Додано спеціальну функцію RGB LED для ввімкнення та зміни поведінки світлодіодів.
* [Налаштування апаратури](bw-radios/radio-settings/radio-setup.md)
  * У **Налаштуваннях GPS** оновлено параметр **Часовий пояс**, щоб дозволити налаштування з 15-хвилинними інтервалами.
  * Додано опцію **Звук запуску**, яка вмикає чи вимикає звук запуску.
  * Додано параметр **Одиниці PPM** - раніше це був варіант збірки.
  * У розділі **Увімкнені функції** додано поточні параметри конфігурації для активної моделі праворуч від перемикача.
  * Додано **Режим обертального енкодера** - **V-N E-I** = вертикальний нормальний, редагування інвертований (інвертується під час редагування тексту).
* [Апаратне забезпечення](bw-radios/radio-settings/hardware.md)
  * Аналогові входи, такі як потенціометри та повзунки, тепер можна налаштувати як **Перемикач**, **Вісь X** або **Вісь Y**. Крім того, їх також можна налаштувати так, щоб вони були _**інвертовані**_.
  * EdgeTX тепер визначатиме під час виконання, чи доступний послідовний порт, щоб дозволити тренер SBUS у відсіку зовнішнього модуля. Якщо так, параметр конфігурації буде доступним.
* Сповіщення
  * Попередження буде відображено, якщо ви спробуєте вимкнути апаратуру, коли підключення тренера все ще активне.
