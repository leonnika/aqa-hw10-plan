# План автоматизации тестирования сценария отправки заявки на открытие вклада "Накопилка" Альфа-Банка.


## 1. Перечень автоматизируемых сценариев

**Сценарий 1:**
№пп | шаги  |ожидаемый результат
--- | --- | ---
1.| Перейти на [веб-сайт Альфа-Банка](https://alfabank.ru/)| Сайт открывается.
2.| Кликнуть по элементу с текстом "Частным лицам"| Надпись "Частным лицам" становиться подчеркнутой.
3.| Навести курсор мыши на пунк (элементу с текстом) "Вклады"| Становится видным меню вкладов.
4.| Кликнуть на пункт (элемент с текстом) "Накопилка"| При клике- переход на страницу с *title* [Накопительный счет «Накопилка» — «Альфа-Банк»](https://alfabank.ru/make-money/savings-account/nakopilka/). При наведении на пункт - текст "Накопилка" меняет цвет на красный. 
5.| Кликнуть на первую кнопку с текстом "Заполнить заявку"| Переход на страницу с *title* [«Накопилка» — «Альфа-Банк»](https://alfabank.ru/make-money/savings-account/nakopilka/anketa/). Появляется текс "Оставьте свои контакты и мы с вами обяхательно свяжемся".
6.|В открывшейся форме, щелкнуть на поле "Имя" (элемент с тегом *name="fio"*)|Поле активно для ввода имени.
7.| *Сценарии тестирования поля "Имя"*
7.1.|Ввести в поле "Имя" имя для обращения| Имя успешно введено. Проверка имени не предусмотрена.
7.2.|Ввести в поле "Имя" имя для обращения| Система позволяет ввод в поле только буквенные символы. Проверка и невозможность ввода цифр и спецюсимволов.
7.3.|Оставить поле "Имя" пустым| Если система не допускает "пустого" поля имени, то выдается сообщние "Заполните Ваше имя для обращения". Если система допускает наличие "пустого" поля имени, то ошибки не возникает.
8.|Щелкнуть по полю "Мобильный телефон"(элемент с тегом *name="mobile"*)|Полеактивно для ввода номера мобильного телефона. Автоматическ заполняютя первые символы +7 
9.|*Сценарии тестирования поля "Мобильный телефон"*
9.1.|Заполнить поле 10-ью цифрами|Номер успешно введен. Кнопка с текстом "Мы перезвоним" активна(при других валидных данных), цвет фона кнопка зеленый.
9.2.|Заполнить поле цифрами в количестве меньше 10|Система выдает ошибку. "Необходимо ввести корректный номер для связи". Или Кнопка "Мы перезвоним" не ативна(При других валидных данных), цвет фона кнопки серый.
9.3.|Заполнить поле цифрами, где первая цифра 0|Система выдает ошибку. "Необходимо ввести корректный номер для связи". Или Кнопка "Мы перезвоним" не ативна(При других валидных данных), цвет фона кнопки серый.
9.4.|Заполнить поле не цифровыми значениями(буквы, спец символы)| Система не допускает ввод не цифровых символов в поле. Или Кнопка "Мы перезвоним" не ативна(При других валидных данных), цвет фона кнопки серый.
9.4.|Оставить поле пустым| Система выдает ошибку "Поле должно быть заполнено". Или Кнопка "Мы перезвоним" не ативна(При других валидных данных), цвет фона кнопки серый.
10.|*Сценарии тестирования флажка "Я согласен(а) на обработку персональных данных"*
10.1|Щелкнуть на флажке согласия (элемент с *class="b-widget_checkbox__checkbox-box"*)| Глалочка успешно выставленна. Кнопка с текстом "Мы перезвоним" активна(при других валидных данных), цвет фона кнопка зеленый.
10.2|Не заполнять флажек согласия| Кнопка "Мы перезвоним" не ативна(При других валидных данных), цвет фона кнопки серый.
11.|Щелкнуть по тексту "персональных данных" у флажка "Я согласен(а) на обработку персональных данных"| Открывается окно (элемент с тегом *data-id="popup_agreement"*) с подробной информацией осогласии. При наведении курсора мышки на текст  "персональных данных" цвет текста становится красным.
12.|Щелкнуть по активной зеленой кнопке с тестом "Мы перезвоним" (кнопка активна при заполненных полях валидными значениями и при установке флажка согласия)| Заявка успешно отправляется. Выходит сообщение с текстом "Спасибо, скоро мы вам перезвоним!" 
<details>
  <summary>Подробнее</summary>

![шаг1](https://github.com/leonnika/aqa-hw10-plan/blob/master/png/%D0%A1%D1%86%D0%B5%D0%BD%D0%B0%D1%80%D0%B8%D0%B91_1.PNG) 

![шаг2](https://github.com/leonnika/aqa-hw10-plan/blob/master/png/%D0%A1%D1%86%D0%B5%D0%BD%D0%B0%D1%80%D0%B8%D0%B91_2.PNG)

![шаг3](https://github.com/leonnika/aqa-hw10-plan/blob/master/png/%D0%A1%D1%86%D0%B5%D0%BD%D0%B0%D1%80%D0%B8%D0%B91_3.PNG)

![шаг4](https://github.com/leonnika/aqa-hw10-plan/blob/master/png/%D0%A1%D1%86%D0%B5%D0%BD%D0%B0%D1%80%D0%B8%D0%B91_4.PNG)

</details>


**Сценарий 2:**
№пп | шаги  |ожидаемый результат
--- | --- | ---
1.| Перейти на [веб-сайт Альфа-Банка](https://alfabank.ru/)| Сайт открывается.
2.| Кликнуть по элементу с текстом "Частным лицам"| Надпись "Частным лицам" становиться подчеркнутой.
3.| Навести курсор мыши на пунк (элементу с текстом) "Вклады"| Становится видным меню вкладов.
4.| Кликнуть на пункт (элемент с текстом) "Накопилка"| При клике- переход на страницу с *title* [Накопительный счет «Накопилка» — «Альфа-Банк»](https://alfabank.ru/make-money/savings-account/nakopilka/). При наведении на пункт - текст "Накопилка" меняет цвет на красный. 
5.| Кликнуть на вторую кнопку с текстом "Заполнить заявку"| Переход на страницу с *title* [«Накопилка» — «Альфа-Банк»](https://alfabank.ru/make-money/savings-account/nakopilka/anketa/). Появляется текс "Оставьте свои контакты и мы с вами обяхательно свяжемся".
6.|Далее шаги 6-12 аналогично сценарию 1.

<details>
  <summary>Подробнее</summary>

![шаг1](https://github.com/leonnika/aqa-hw10-plan/blob/master/png/%D0%A1%D1%86%D0%B5%D0%BD%D0%B0%D1%80%D0%B8%D0%B91_1.PNG) 

![шаг2](https://github.com/leonnika/aqa-hw10-plan/blob/master/png/%D0%A1%D1%86%D0%B5%D0%BD%D0%B0%D1%80%D0%B8%D0%B92_2.PNG)

![шаг3](https://github.com/leonnika/aqa-hw10-plan/blob/master/png/%D0%A1%D1%86%D0%B5%D0%BD%D0%B0%D1%80%D0%B8%D0%B91_3.PNG)

![шаг4](https://github.com/leonnika/aqa-hw10-plan/blob/master/png/%D0%A1%D1%86%D0%B5%D0%BD%D0%B0%D1%80%D0%B8%D0%B91_4.PNG)

</details>

**Сценарий 3:**
№пп | шаги  |ожидаемый результат
--- | --- | ---
1.|Перейти на [веб-сайт Альфа-Банка](https://alfabank.ru/)|Сайт открывается.
2.|Кликнуть по элементу с текстом "Частным лицам"| Надпись "Частным лицам" становиться подчеркнутой.
3.|Кликнуть по элементу с текстом "Вклады"| Переход на страницу с *title* [Депозиты — «Альфа-Банк»](https://alfabank.ru/make-money/deposits/).
4.|Кликнуть по элементу с текстом "Накопительные счета"|Переход на страницу с *title* [Накопительные счета — «Альфа-Банк»](https://alfabank.ru/make-money/savings-account/).
5.|Кликнуть по элементу на странице с описанием вклада с текстом "Максимальный процент на любую сумму Накопилка" | Переход на страницу с *title* [Накопительный счет «Накопилка» — «Альфа-Банк»](https://alfabank.ru/make-money/savings-account/nakopilka/?submitted=true&limit_rub=10000000&currency=rub&period=0). При наведении курсоора на текст "Максимальный процент на любую сумму" становится красным цветом.
6.|Кликнуть на первую кнопку с текстом "Заполнить заявку"| Переход на страницу с *title* [«Накопилка» — «Альфа-Банк»](https://alfabank.ru/make-money/savings-account/nakopilka/anketa/). Появляется текс "Оставьте свои контакты и мы с вами обяхательно свяжемся"
7.|Далее шаги 7-12 аналогично сценарию 1.

<details>
  <summary>Подробнее</summary>

![шаг1](https://github.com/leonnika/aqa-hw10-plan/blob/master/png/%D0%A1%D1%86%D0%B5%D0%BD%D0%B0%D1%80%D0%B8%D0%B93_1.PNG) 

![шаг2](https://github.com/leonnika/aqa-hw10-plan/blob/master/png/%D0%A1%D1%86%D0%B5%D0%BD%D0%B0%D1%80%D0%B8%D0%B93_2.PNG)

![шаг3](https://github.com/leonnika/aqa-hw10-plan/blob/master/png/%D0%A1%D1%86%D0%B5%D0%BD%D0%B0%D1%80%D0%B8%D0%B91_2.PNG)

![шаг4](https://github.com/leonnika/aqa-hw10-plan/blob/master/png/%D0%A1%D1%86%D0%B5%D0%BD%D0%B0%D1%80%D0%B8%D0%B91_3.PNG)

![шаг5](https://github.com/leonnika/aqa-hw10-plan/blob/master/png/%D0%A1%D1%86%D0%B5%D0%BD%D0%B0%D1%80%D0%B8%D0%B91_4.PNG)

</details>

**Сценарий 4:**
№пп | шаги  |ожидаемый результат
--- | --- | ---
1.|Перейти на [веб-сайт Альфа-Банка](https://alfabank.ru/)|Сайт открывается.
2.|Кликнуть по элементу с текстом "Частным лицам"| Надпись "Частным лицам" становиться подчеркнутой.
3 |Кликнуть по элементу с текстом "Вклады"| Переход на страницу с *title* [Депозиты — «Альфа-Банк»](https://alfabank.ru/make-money/deposits/).
4.|Кликнуть по элементу с текстом "Накопительные счета"|Переход на страницу с *title* [Накопительные счета — «Альфа-Банк»](https://alfabank.ru/make-money/savings-account/).
5.|Кликнуть по элементу на странице с описанием вклада с текстом "Максимальный процент на любую сумму Накопилка" | Переход на страницу с *title* [Накопительный счет «Накопилка» — «Альфа-Банк»](https://alfabank.ru/make-money/savings-account/nakopilka/?submitted=true&limit_rub=10000000&currency=rub&period=0). При наведении курсоора на текст "Максимальный процент на любую сумму" становится красным цветом.
6.|Кликнуть на вторую кнопку с текстом "Заполнить заявку"| Переход на страницу с *title* [«Накопилка» — «Альфа-Банк»](https://alfabank.ru/make-money/savings-account/nakopilka/anketa/). Появляется текс "Оставьте свои контакты и мы с вами обяхательно свяжемся"
7.|Далее шаги 7-12 аналогично сценарию 1.

<details>
  <summary>Подробнее</summary>

![шаг1](https://github.com/leonnika/aqa-hw10-plan/blob/master/png/%D0%A1%D1%86%D0%B5%D0%BD%D0%B0%D1%80%D0%B8%D0%B93_1.PNG) 

![шаг2](https://github.com/leonnika/aqa-hw10-plan/blob/master/png/%D0%A1%D1%86%D0%B5%D0%BD%D0%B0%D1%80%D0%B8%D0%B93_2.PNG)

![шаг3](https://github.com/leonnika/aqa-hw10-plan/blob/master/png/%D0%A1%D1%86%D0%B5%D0%BD%D0%B0%D1%80%D0%B8%D0%B92_2.PNG)

![шаг4](https://github.com/leonnika/aqa-hw10-plan/blob/master/png/%D0%A1%D1%86%D0%B5%D0%BD%D0%B0%D1%80%D0%B8%D0%B91_3.PNG)

![шаг5](https://github.com/leonnika/aqa-hw10-plan/blob/master/png/%D0%A1%D1%86%D0%B5%D0%BD%D0%B0%D1%80%D0%B8%D0%B91_4.PNG)

</details>


## Перечень используемых инструментов с обоснованием выбора
1. Браузер Google Chrome v.83.0.4103.97
*Наиболее частоиспользуемый браузер. Множество инструментов для UI тестирования  и разработки*
2. OpenJDK 11 (LTS)
*Актуальная версия. Проект по созданию полностью совместимого Java Development Kit, состоящего исключительно из свободного и открытого исходного кода.*

3. IntelliJ IDEA 2019.2.4 (Community Edition)
*Интеллектуальная мощная среда разработки на JAVA и не только, понимающая код. Обращает внимание на существующие ошибки и самостоятельно устраняет их, предоставляет варианты автоматического дополнения кода,избавляет от повседневной рутины и позволяет сконцентрироваться на более важных задачах.*

4. Библиотека для модульного тестирования Junit-jupiter v.5.6.1 
 *JUnit 5 состоит из JUnit Platform ,JUnit Jupiter, JUnit Vintage(позволяет интегрировать предедущие версии). Предназначена библиотека для модульного тестирования программного обеспечения на языке Java. Это актуальная версия библиотеки тестирования. Принципиальных различий по описанию возможностей от TestNG не найдено.* 

5. Selenide v.5.12.0.
*Selenide - удобный инструмент для автоматических тестов, построенный на базе Selenium WebDriver. Он позволяет автоматически управлять браузером (открытие, закрытие).Selenide предлагает лаконичный и мощный API, который поможет писать короткие и хорошо читаемые тесты.Когда тест падает, Selenide автоматически делает скриншот.*

6. Проект на базе сборки Gradle. 
*Gradle ряд плюсов. Скрипты сборки Gradle, написанные на Groovy, на порядок короче XML, используемых Maven. Работа с командной строкой быстрее и проще. Проще подключение зависимостей. Gradle быстрее Maven, в нём используются всевозможные кэши и даже специальный процесс – Gradle Daemon, живущий после сборки.*

## Перечень необходимых разрешений/данных/доступов от банка 
В ходе позитивного тестирования по разным сценариям осуществляются отправки заявок на открытие вклада. При тестировании на реальном сайте банка, эти заявки будут отрабатываться специалистами Альфа банка. Следовательно, было бы рациональнее тестировать отправку таких заявок на тестовом варианте сайта без дальнейшей обработке заявок специалистами. 

## Перечень и описание возможных рисков при автоматизации
В ситуации если графический интерфейс части сайта, отвечающего за создание заявки, сильно изменится в ближайшем будущем, то возникают большие риски обрушения всех созданных ранее веб-тестов. Следовательно при любых изменениях UI сайта, необходимо актуализировать все автотесты.

## Перечень необходимых специалистов для автоматизации и интервальная оценка с учётом рисков (в часах)
Требования к специалистам для автоматизации:

*hard skills*
* Свободное владения всеми инструментами, которые указаны в перечне данного плана выше.
* Знание и понимание теоретических основ процесса тестирования.

*soft skills*
* Аккуратность и внимательность к деталям.

Количество специалистов для автоматизации зависит от сроков, за которые нужно выполнить автоматизацию. Ориентировочно для автоматизации одного сценария создания заявки одним специалистом необходимо 1-1,5 часа . На автоматизацию всех сценариев потребуется 4-6 часов одному специалисту. Плюс нужно заложить около 1 часа на составление отчета по результатам автоматизации (при необходимости).Если нет временных ограничений, то потребуется один специалист для осуществления автоматизации тестирования и составления отчета. 




