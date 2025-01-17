# Система бронирования парковки "ParkApp"

**Архитектор**: Иван Иванов / Название организации  
**КОНФИДЕНЦИАЛЬНО**
**Дата:** 17 Августа 2023


### Содержание

### История версий

> ***Опционально***  
> Отражает изменения, внесенные в документ, включая дату, версию, описание изменения и автора

| Дата | Автор | Что изменилось | 
| :-: | :-: | :-: |
| 16.08.2023| Иван Иванов | Все | 

### Краткий обзор

> Краткий обзор всей архитектуры решения. Должен предоставлять общее представление о целях проекта, ключевых особенностях, основных преимуществах, ожидаемых затратах и потенциальных рисках. Главным образом предназначено для лиц, принимающих решения, которые могут не углубляться в детальные разделы документа.

##### Название проекта: ПЛАТФОРМА ОНЛАЙН-РИТЕЙЛА NEXTGEN 

Современный рынок электронной коммерции требует скорости, гибкости и ориентированного на пользователя подхода. 
Проект "Платформа онлайн-ритейла NextGen" - это наш стратегический ответ на эти требования, гарантируя, что мы не только соответствуем текущим стандартам рынка, но и готовы к будущим изменениям в онлайн-ритейле. 

##### Цель

Переход от нашей устаревшей системы онлайн-продаж к надежной, масштабируемой и дружелюбной платформе, которая улучшает опыт покупателя, безупречно интегрируется с нашими системами управления цепочкой поставок и поддерживает ожидаемый рост в течение следующих пяти лет. 

##### КЛЮЧЕВЫЕ ОСОБЕННОСТИ

- ***АДАПТИВНЫЙ ВЕБ-ДИЗАЙН:*** Обеспечивает оптимальный просмотр на различных устройствах, от мониторов компьютера до мобильных телефонов.
- ***ИНТЕГРИРОВАННАЯ СИСТЕМА РЕКОМЕНДАЦИЙ НА ОСНОВЕ ИСКУССТВЕННОГО ИНТЕЛЛЕКТА:*** Персонализирует покупательский опыт, предлагая продукты на основе истории просмотров и покупок. 
- ***БЕСШОВНАЯ ИНТЕГРАЦИЯ С ПЛАТЕЖНЫМИ СИСТЕМАМИ:*** Предлагает множество вариантов оплаты, улучшая процесс оформления заказа. 
- ***ПРЕИМУЩЕСТВА:*** Ожидаемый рост онлайн-продаж на 25% благодаря улучшенному пользовательскому опыту. Снижение числа за счет оптимизации процесса оформления. Расширенные возможности аналитики данных, предоставляющие информацию о поведении и предпочтениях клиентов. 
- ***ОРИЕНТИРОВОЧНАЯ СТОИМОСТЬ:*** Общие инвестиции в этот переход оцениваются в $1,2 млн, с прогнозируемой окупаемостью инвестиций в 40% в течение следующих трех лет. 
- ***РИСКИ:*** Возможные краткосрочные перебои во время перехода от устаревшей системы. Необходимость обучения персонала новой платформе. 

Платформа онлайн-ритейла NextGen - это не просто технологическое обновление, это инвестиции в наше будущее, гарантируя, что мы останемся на передовой инноваций в области электронной коммерции и продолжим эффективно обслуживать наших клиентов.

### Введение

> В этом разделе представлена ключевая терминология по архитектуре решения и границы проекта. Он разработан для того, чтобы все заинтересованные стороны имели общее понимание, и не было двусмысленностей в терминах или границах проекта.

### Ключевые термины, определения, аббревиатуры

> ***Опционально***  
> Представляет любую специализированную терминологию, сокращения или аббревиатуры, используемые в документе. Это помогает обеспечить ясность и понимание для всех заинтересованных сторон.

| Термин | Определение |
|:-:|:-|
| СУБД | Система управления базами данных |

### Границы проекта

> Четко определяет, что включено в проект, и, что не менее важно, что исключено. Это устанавливает четкие границы для целей проекта, результатов, функций и функциональных возможностей.

##### Включено: 
- Разработка нового интерфейса платформы электронной коммерции. 
- Интеграция системы рекомендаций на основе искусственного интеллекта. 
- Перенос существующих пользовательских данных в новую систему. 
##### Исключено: 
- Пересмотр системы управления цепочкой поставок на бэкенде. 
- Разработка нового мобильного приложения.

### Требования

> В этом разделе рассматриваются конкретные требования к проекту, кто в нем участвует и контекст, в котором решение будет разработано и предоставлено.

#### Заинтересованные стороны

> Определяет и описывает основные группы или отдельных лиц, которые заинтересованы/участвуют в проекте, его результатах или затрагиваются его итогами. Важно понимать их потребности, опасения и влияние. 

> [!NOTE]
>  - **Сторона:** Указывает на группу или категорию, к которой принадлежит заинтересованная сторона. Это может быть отдел, группа пользователей или внешняя организация. 
>  - **Имя:** Если применимо, это было бы конкретное лицо, представляющее сторону-участника, особенно актуально для ключевых лиц, принимающих решения, или основных контактных лиц. 
>  - **Роль/Должность:** Определяет основную функцию или отношение участника к проекту. 
>  - **Интересы/Опасения:** Описывает конкретные интересы, риски или потребности, которые участник может иметь в отношении проекта.

| Сторона | Имя | Роль/Должность | Интересы/Опасения |
| :-: | :-: | :-: | :- |
| Инженерная команда | Иван Иванов | Архитектор | Согласованные и подробно описанные требования |

#### Функциональные требования

> Описывает конкретные функциональные возможности, которые система должна предоставлять в четких, выполнимых терминах.

> [!NOTE]
> - **Группа:** Категория или модуль, к которому принадлежит функциональное требование. 
> - **ID:** Уникальный идентификатор для каждого требования. Это помогает в отслеживании, ссылке и управлении требованием на протяжении всего его жизненного цикла. 
> - **Описание:** Четкое и подробное изложение требования, объясняющее, какая конкретная функциональность или поведение ожидается.
> - **Приоритет:** Определяет важность требования по отношению к другим требованиям. Обычно используются уровни **ВЫСОКИЙ**, **СРЕДНИЙ** и **НИЗКИЙ**. Другие шкалы, такие как **MOSCOW (ОБЯЗАТЕЛЬНО, ЖЕЛАТЕЛЬНО, ВОЗМОЖНО, НЕ ТРЕБУЕТСЯ)**, также могут быть использованы в зависимости от организационных предпочтений.

| Группа | ID | Описание | Приоритет |
| :-: | :-: | :- | :-: |
| Корзина покупок | FR-001 | Должна работать как корзина покупок | Высокий |

#### Нефункциональные требования

> Охватывает качество или критерии функционирования системы, такие как производительность, масштабируемость и безопасность.

> [!NOTE]
> - **Группа:** Категория или атрибут качества, к которому принадлежит нефункциональное требование ([список общих атрибутов качества для использования:](https://en.wikipedia.org/wiki/List_of_system_quality_attributes))
> - **ID:** Уникальный идентификатор для каждого требования.
> - **Описание:** Четкое и подробное изложение требования.
> - **Приоритет:** Определяет важность требования по отношению к другим требованиям. Обычно используются уровни **ВЫСОКИЙ**, **СРЕДНИЙ** и **НИЗКИЙ**. Другие шкалы, такие как **MOSCOW (ОБЯЗАТЕЛЬНО, ЖЕЛАТЕЛЬНО, ВОЗМОЖНО, НЕ ТРЕБУЕТСЯ)**, также могут быть использованы в зависимости от организационных предпочтений.

| Группа | ID | Описание | Приоритет |
| :-: | :-: | :- | :-: |
| Responsiveness | NFR-001 | Время реакции системы для 95% действий пользователей не должно превышать 2 секунды | Высокий |

#### Ограничения

> Перечисляются ограничения, в рамках которых должна работать команда проекта, такие как технологические, финансовые или временные ограничения.

> [!NOTE]
> - **Тип:** Категория или характер ограничения, например: техническое, финансовое, временное и т. д.
> - **ID:** Уникальный идентификатор для каждого ограничения
> - **Описание:** Четкое и подробное описание ограничения.

| Тип | ID | Описание |
| :-: | :-: | :- |
| Техническое | C-001 | Новая платформа должна быть обратно совместима с существующей системой CRM. |
| Финансовое | С-002 | Проект не должен превышать бюджет в $1 млн. |
| Временное | C-003 | Развертывание должно быть завершено до начала предпраздничного сезона покупок, т.е. до 1 ноября. |

#### Предположения

> Документируются все предполагаемые факты или условия, которые будут влиять на решения проекта. Они часто служат основой для рисков, так как предположения часто включают в себя некоторую степень неопределенности.

> [!NOTE]
> - **ID:** Уникальный идентификатор для каждого предположения для легкого его учета.
> - **Описание:** Четкое и краткое изложение предположения.

| ID | Описание |
| :-: | :- |
| A-001 | Пользовательский трафик не увеличится более чем на 30% в первые шесть месяцев после развертывания. |
| A-002 | Существующая IT-команда обладает необходимыми навыками для поддержки и обслуживания новой платформы. |
| A-003 | Сторонние поставщики предоставят необходимую документацию по API вовремя. |

---
### Текущая архитектура

>***Опционально***
>Этот раздел предоставляет подробное описание текущего состояния архитектуры. Для обеспечения последовательности в представлении и упрощения сравнения с "Целевой архитектурой" рекомендуется использовать те же разделы/подразделы, что и в "Целевой архитектуре".

---
### Целевая архитектура

>Этот раздел предоставляет всесторонний взгляд на предлагаемую архитектуру системы, учитывая как технические, так и бизнес-аспекты. Он включает в себя детали компонентов системы, их взаимоотношений, потока данных и других архитектурных аспектов, необходимых для достижения целей проекта.

##### Обзор

>Краткое резюме общей целевой архитектуры, создающее основу для более подробных представлений, которые следуют далее.

##### Функциональное Представление

>***Опционально***  
>Описывает функциональные элементы системы, их обязанности, взаимодействия и отношения.

##### Развертывание

>***Опционально***  
>Описывает физическое и виртуальное развертывание программных компонентов, учитывая аспекты масштабирования, распределения и механизмов отказоустойчивости.

##### Процессы

>***Опционально***  
>Описывает динамическое поведение системы, изображая параллельные процессы, синхронизацию и последовательность событий.

##### Данные

>***Опционально***  
>Описывает аспекты данных системы, включая модели данных, механизмы хранения, отношения и потоки данных.

##### Безопасность

>***Опционально***  
>Описывает меры и стратегии для обеспечения безопасности системы. Это может включать в себя детали об аутентификации, авторизации, шифровании, обнаружении вторжений и т. д.

##### Производительность

>***Опционально***  
>Описывает стратегии для достижения желаемых показателей производительности. Это может охватывать аспекты, такие как задержка, пропускная способность, распределение нагрузки и техники оптимизации.

##### Сетевое взаимодействие

>***Опционально***  
>Описывает аспекты связи, топологии сети и протоколы, учитывая пропускную способность, задержку и другие сетевые факторы.

---
### Альтернативные варианты

>***Опционально***  
>В этом разделе описываются альтернативные решения или архитектуры, которые рассматривались на этапе планирования. Детализация этих вариантов и причины их невыбора помогают обеспечить ясность и прозрачность в процессах принятия решений.

##### 1. Развертывание на собственных серверах
- **Описание:** Основные характеристики и особенности этой альтернативы.
- **Преимущества:** Преимущества или сильные стороны.
- **Ограничения:** Возможные проблемы или недостатки.
- **Причина отказа от варианта:** Объяснение, почему этот вариант не был выбран.
##### 2. Гибридное облачное решение
- **Описание:** Основные характеристики и особенности этой альтернативы.
- **Преимущества:** Преимущества или сильные стороны.
- **Ограничения:** Возможные проблемы или недостатки.
- **Причина отказа от варианта:** Объяснение, почему этот вариант не был выбран.

##### Критерии оценки

>***Опционально***  
>Опишите метрики или критерии, используемые для оценки каждого варианта. Это может включать в себя стоимость, масштабируемость, простоту внедрения, совместимость с существующими системами и т. д.

##### Итог

>***Опционально***  
>Заключение об рассмотренных альтернативах и причин, по которым было принято окончательное решение. В этом разделе также можно указать любые планы по повторному рассмотрению этих альтернатив в будущем, если это актуально.

---
### Риски

>Этот раздел описывает потенциальные риски, которые могут повлиять на успешную реализацию или функционирование решения. Риски следует регулярно пересматривать, переоценивать и обновлять по мере продвижения проекта. Для каждого риска следует предоставить стратегии смягчения и реагирования.

> [!NOTE]
> - **ID Риска:** Уникальный идентификатор для каждого риска для легкого его учета (например, R-001).
> - **Описание:** Краткое описание риска.
> - **Влияние:** Серьезность риска в случае его реализации. Обычно оценивается как НИЗКОЕ, СРЕДНЕЕ, ВЫСОКОЕ или КРИТИЧНОЕ.
> - **Вероятность:** Вероятность возникновения риска. Обычно категоризируется как НИЗКАЯ, СРЕДНЯЯ или ВЫСОКАЯ. 
> - **Стратегия смягчения:** Проактивные меры, принимаемые для предотвращения или снижения вероятности или воздействия риска.
> - **Стратегия реагирования:** Реактивные меры, запланированные на случай реализации риска.

| ID Риска | Описание | Влияние | Вероятность | Стратегия смягчения | Стратегия реагирования |
| :-: | :- | :-: | :-: | :- | :- |
| R-001 | Задержка в получении необходимых лицензий на программное обеспечение | Низкая | Средняя | Договориться и утвердить лицензии до начала разработки | Иметь резервный список альтернативного программного обеспечения или инструментов |

---

### Бюджет и дорожная карта

>Этот раздел предоставляет стратегический взгляд на то, как будет внедрено решение, детализируя ключевые этапы и планируемые действия на пути. Это выравнивает ожидания и предоставляет основу для отслеживания и измерения прогресса.

#### Дорожная карта

>Для представления временной шкалы проекта можно использовать диаграмму Ганта высокого уровня или аналогичный визуальный инструмент. На нем следует выделить основные этапы, действия и соответствующие временные рамки. Если предполагается фазовый подход, укажите фазы и связанные с ними действия.

#### Планирование ресурсов

> В этом подразделе следует подробно описать необходимые ресурсы, как в плане рабочей силы, так и в плане инфраструктуры. Укажите роли, необходимые навыки и оцененные затраты в человеко-часах или человеко-днях. Не забудьте включить ресурсы для деятельности, не связанной с разработкой, такой как обучение, документация и поддержка. 

| Роль | Цена за месяц (USD) | Янв | Фев | Мар | Апр | Май | Июн | Итог (USD) |
| :- | -: | -: | -: | -: | -: | -: | -: | :-: |
|**Архитектор Решений**|$10,000|0.4|0.4|0.2|0.2|-|-|$22,000|
|**Бизнес Аналитик**|$8,000|0.8|0.7|0.6|0.5|0.3|0.2|$42,600|
|**Разработчик (Backend)**|$7,500|2.0|2.0|2.0|2.0|2.0|2.0|$90,000|
|**Разработчик (Frontend)**|$7,000|1.0|1.0|1.0|1.0|1.0|1.0|$42,000|
|**DevOps**|$8,000|0.5|1.0|1.0|0.2|0.2|0.2|$25,600|
|**Дизайнер**|$6,500|0.7|0.8|0.5|0.5|0.2|-|$26,450|
|**Проектный Менеджер**|$9,000|0.5|0.5|0.5|0.5|0.5|0.5|$32,40|
|**Тестировщик**|$7,200|$32,40|$32,40|$32,40|$32,40|$32,40|$32,40|$41,760|

Предполагаемый общий бюджет на разработку SaaS MVP в течение 6 месяцев, на основе подробного распределения ресурсов, составляет $323,810
