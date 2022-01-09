# NISProject
Проект веб-приложения для создания плейлистов с системой рекомендаций в рамках Научно-исследовательского семинара

## Содержание
* [Описание доменной области](https://github.com/CyrilHaritonov/NISProject/blob/main/README.md#%D0%BE%D0%BF%D0%B8%D1%81%D0%B0%D0%BD%D0%B8%D0%B5-%D0%B4%D0%BE%D0%BC%D0%B5%D0%BD%D0%BD%D0%BE%D0%B9-%D0%BE%D0%B1%D0%BB%D0%B0%D1%81%D1%82%D0%B8)
* [Описание Use-Case](https://github.com/CyrilHaritonov/NISProject/blob/main/README.md#%D0%BE%D0%BF%D0%B8%D1%81%D0%B0%D0%BD%D0%B8%D0%B5-use-case)
* [Функциональные и не функциональные требования](https://github.com/CyrilHaritonov/NISProject/blob/main/README.md#%D1%84%D1%83%D0%BD%D0%BA%D1%86%D0%B8%D0%BE%D0%BD%D0%B0%D0%BB%D1%8C%D0%BD%D1%8B%D0%B5-%D0%B8-%D0%BD%D0%B5-%D1%84%D1%83%D0%BD%D0%BA%D1%86%D0%B8%D0%BE%D0%BD%D0%B0%D0%BB%D1%8C%D0%BD%D1%8B%D0%B5-%D1%82%D1%80%D0%B5%D0%B1%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D1%8F)
* [Архитектура](https://github.com/CyrilHaritonov/NISProject/blob/main/README.md#%D0%B0%D1%80%D1%85%D0%B8%D1%82%D0%B5%D0%BA%D1%82%D1%83%D1%80%D0%B0)

## Описание доменной области


### A.	Цель.

Целью данного веб-приложения явлеяется выдача подходящих рекомендаций для дополнения музыкального плейлиста.

### B.	Определения.

Плейлист - подборка аудио-контента для воспроизведения на радио или с помощью медиаплеера.

Рекомендованный трек – трек, который система рекомендаций считает подходящим для включения на определенную позицию плейлиста.

Система рекомендаций – система, которая по информации о плейлисте может рекомендовать треки для его дополнения.

### C. Основыне задачи, которые должно выполнять приложние.

•	Удовлетворение потребности пользователя к отрытию новой музыки, так как это является одной из ключевых причин продления подписки на стриминговые сервисы. [1]

•	Учитывание контекста использования плейлиста и цель создания плейлиста, так как они играют ключевую роль в восприятии музыки.[2] 

•	Простота использования, так как сложность использования системы является распространненной причиной неиспользования системы рекомендаций. [2]

•	Определение цели и контекста, в котором будет использован плейлист, так как это снижает сложность его составления. [2]

•	Эффективное использование алгоритма RAGH, так как представленные алгоритмом RAGH, показались пользователям предпочтительнее тех, что были представлены алгоритмом рекомендаций Spotify. [2]

•	Возможность изменения порядка, в котором идут треки, для составления плейлиста. Существующие системы рекомендаций не берут в расчет позицию в плейлисте, на которую подбирается трек. [2]

### D.	Клиенты и пользователи

Потенциальными клиентами могут быть обычные пользователи стриминговых сервисов желающие получить улучшенное качество рекомендаций при создании плейлистов, либо же стриминговые сервисы, которые захотят использовать данную систему в своем приложении.


### E.	Среда

Пользователи пользуются стриминговыми сервисами используя как мобильные устройства, так и персональные компьютеры и ноутбуки, смарт тв и умные часы.
Спектр устройств, с которых пользователь может воспользоваться стриминговым сервисом, постоянно растет.
 
### F.	Задачи и действия, которые производятся сейчас.

Пользователь использует рекомендации при создании плейлистов, которые не учитывают контекст и цель создания плейлиста, подбирают треки в независимости от порядка, в котором идут треки.

### G.	 Конкурирующее программное обеспечение.

Большинство стриминговых сервисов уже имеют в своем составе системы рекомендаций при создании плейлистов. Несмотря на это, эти системы содержат в себе ряд недостатков, так они не учитывают контекст и цель создания плейлиста, порядок в котором идут треки, зачастую использую менее эффективные алгоритмы для подбора треков.

### H.	Схожести с другими доменными областями.

У систем рекомендаций треков при создании плейлистов есть схожести с системами рекомендаций треков, которые создают готовые плейлисты для пользователя, основываясь на его предпочтениях, в них используются схожие алгоритмы подбора треков.

### I.	Ссылки на использованные материалы.

1.	Mäntymäki, Matti & Islam, A.K.M. Najmul (2015) “Gratifications from using freemium music streaming services: Differences between basic and premium users” In proceedings of the International Conference on Information Systems (ICIS2105)
2.	Kamehkhosh, I., Bonnin, G. & Jannach, D. Effects of recommendations on the playlist creation behavior of users. User Model User-Adap Inter 30, 285–322 (2020).

## Описание Use-Case

### Пример 1. Создание плейлиста.
Действующие лица: пользователь, система рекомендаций.

Цель: создать плейлист.

Предусловие: у пользователя не израсходован лимит на создание плейлистов.

Успешный сценарий:
1.	Пользователь выбирает контекст из списка предложенных.
2.	Пользователь выбирает первый трек вручную использую поиск.
3.	Система рекомендаций выдает треки для дополнения текущего плейлиста.
4.	Пользователь выбирает трек либо из рекомендаций, либо самостоятельно через поиск и добавляет его в плейлист.
5.	Если был выбран трек из рекомендаций, то информация о его выборе передается в систему, чтобы использовать ее для выдачи новых рекомендаций, иначе (5).
6.	Пользователь завершает процесс заполнения плейлиста.

Альтернативные сценарии:
* Предусловие не выполнено: Если у пользователя израсходован лимит на создание плейлистов, то приложение выдает ошибку с соответствующим описанием.
* (5) Если трек был выбран самостоятельно через поиск, то информация о его выборе передается в систему, но также информация о невыбранных среди рекомендаций треках тоже передается в систему.

### Пример 2. Экспорт плейлиста.
Действующие лица: пользователь, система, стриминговый сервис.

Цель: экспортировать плейлист в стриминговый сервис.

Предусловие: в системе есть плейлист, созданный пользователем до этого.

Успешный сценарий:
1.	Пользователь выбирает плейлист, который хочет экспортировать среди плейлистов, созданных им до этого.
2.	Пользователь выбирает стриминговый сервис, в который будет экспортирован плейлист.
3.	Пользователь входит в аккаунт в данном стриминговом сервисе (если уже не был залогинен, то (3))
4.	Система составляет в стриминговом сервисе плейлист с содержанием аналогичным экспортируемому плейлисту.
5.	Пользователь имеет доступ к экспортированному плейлисту в своем аккаунте в стриминговом сервисе.

Альтернативные сценарии:
* (3) Переходим к use-case 5.
### Пример 3. Покупка подписки.
Действующие лица: пользователь, система, платежная система.

Цель: приобрести подписку.

Предусловие: у пользователя есть аккаунт в системе.

Успешный сценарий:
1.	Пользователь нажимает кнопку ответственную за переход в систему покупки подписки.
2.	Пользователь выбирает условия подписки (если такие есть).
3.	Пользователь вводит информацию необходимую для совершения покупки и совершает покупку.
4.	Система получает информацию о совершенной покупке от платежной системы.
5.	Система меняет статус состояния подписки пользователя на активный.

Альтернативные сценарии:
* (4) Если система покупки не передала информацию о совершении покупки за промежуток времени выделенный на оплату, то выдать ошибку.
### Пример 4. Регистрация в системе.
Действующие лица: система, пользователь, система регистрации.

Цель: создать аккаунт в системе.

Успешный сценарий:
1.	Пользователь нажимает кнопку, которая открывает систему регистрации.
2.	Система предлагает пользователю ввести данные для создания аккаунта (email, login, password etc.), система сразу же проверяет их корректность(делает простейший проверки, финальные проверки(на наличие аккаунта с такими данными) уже делает back-end), в случае не корректности выдает ошибку.
3.	Система также предлагает пользователю войти в аккаунт в стриминговом сервисе.
4.	Пользователь вводит информацию/входит в аккаунт в стриминговом сервисе.
5.	Система создает аккаунт используя введенную информацию/данные аккаунта стримингового сервиса.
6.	Если они некорректны, то возвбращаемся в пункт 2.

### Пример 5. Вход в аккаунт.
Действующие лица: пользователь, система логина.

Цель: войти в аккаунт.

Предусловие: наличие у пользователя данных для логина.

Успешный сценарий:
1.	Система предлагает пользователю войти в существующий аккаунт/ создать новый.
2.	Пользователь выбирает войти в существующий аккаунт.
3.	Открывается система логина.
4.	Пользователю предложено ввести данные для логина.
5.	Пользователь вводит данные.
6.	Система проверяет наличие пользователя с такими данными в БД.
7.	Пользователь залогинен в систему, иначе возварщаемся в пункт 3.

## Функциональные и не функциональные требования

### Функциональные требования:

*	В веб-приложении должен быть реализован полный функционал регистрации и авторизации:
    *	 Должна быть возможность создать аккаунт, используя либо вводимую пользователем информацию (email, логин, пароль), либо информацию предоставляемую стриминговым сервисом через аккаунт, в котором пользователь авторизировался в системе регистрации.
    *	Должа быть возможность войти в веб-приложение используя данные от заранее созданного аккаунта, либо аккаунт в стриминговом сервисе, с использованием, которого был создан аккаунт в веб-сервисе.
    *	В веб-приложении должен быть функционал смены пароля, почты существующего аккаунта.
    *	В веб-приложении должна быть возможность выйти из аккаунта, в который на данный момент произведен вход.
*	В веб-приложении должен быть реализован функционал поиска треков.
    *	Поиск трека используя его название и название исполнителя.
    *	Добавление трека в плейлист.
*	В веб-приложении должен быть реализован функционал связанный с плейлистами:
    *	Создание пользователем нового плейлиста.
    *	Возможность указать контекст, в котором будет использован плейлист и цель создания плейлиста.
    *	Редактирование пользователем существующего плейлиста.
    *	Удаление существующего плейлиста.
    *	Экспорт плейлиста в стриминговый сервис, выбранный пользователем.
    *	Добавление и удаление треков внутри плейлиста, изменение порядка в котором они идут.
    *	Веб-приложение должно хранить статистику о количестве плейлистов которое пользователь создал за месяц.
*	В веб-приложении должен быть реализован функционал, связанный с выдачей рекомендаций при создании плейлиста:
    *	Вывод предложенных на последнюю позицию в текущем плейлисте треков.
    *	Возможность убрать определённый трек или исполнителя из рекомендаций.
    *	Вывод предложенных на заданную пользователем позицию треков.
    *	Предложенные треки должны обладать 30-секундными превью.
    *	При выдаче новых рекомендаций должны учитываться предыдущие выборы, сделанные пользователем.
    *	Выдача рекомендаций не должна занимать время дольше 3-х секунд.
*	В веб-приложении должен быть функционал связанные с платной подпиской:
    *	Возможность приобрести подписку, используя платежную карту.
    *	Возможность отменить подписку.
    *	Платная подписка должна разблокировать доступ к части функционала приложения.
*	В веб-приложении должна быть панель администратора:
    *	В панеле администратора должна быть возможность менять функционал доступный пользователю по подписке: расширять его и ограничивать.
### Нефункциональные требования:

*	Веб-страница с веб-приложением должна загружаться до работоспособного состояния в двух секунд при первом запуске и быстрее секунды при последующих.
*	Итоговое веб-приложение должно работать в актуальных версиях популярных браузеров.
*	Веб-приложение должно иметь адаптивный интерфейс, в частности должно быть адаптировано для экранов мобильных устройств.
*	В веб-приложении должна быть возможность найти через поиск все треки из библиотеки Spotify.
*	Данные пользователя (плейлисты созданные пользователем, выборы, сделанные пользователем при добавлении треков в плейлист) должны храниться в облачном сервисе, чтобы пользователь имел доступ к ним вне зависимости от устройства, с которого он использует веб-приложение.
*	В веб-приложении должна быть возможность экспорта созданных плейлистов в крупнейшие стриминговые сервисы.
*	Система рекомендаций должна использовать алгоритм RAGH для подбора треков.
*	В системе рекомендаций должен использоваться API Spotify для выполнения запросов связанных с поиском треков, получении информации о них.
*	Для покупки подписки должна быть использована онлайн касса с широким выбором средств оплаты.
*	Серверная часть приложения должна быть развернута в Microsoft Azure
*	Должен использоваться Docker
*	В случае ошибки система должна быть снова работоспособона в течении пяти минут.
*	Пользовательский интерфейс должен соответствовать ["User Interface Guidelines for Web-Applications"](https://www.designyup.com/7-user-interface-design-guidelines-for-web-applications/)

## Архитектура

 ![Component Diagram](img/componentDiagram.png)

### Референсная архитектура

![Reference Architecture](img/referenceArchitecture.png)
 
### Основные компоненты
* Data Base
* Data Uploader
* Reqeust Handler
* RAGH Module
* Al Module
* User Data Module
* Spotify API
* Web-App

### Описание компонентов
* Data Base - база данных, содержащая в себе информацию о пользователях и их плейлистах
* Data Uploader - добавляет, удаляет, редактирует, считывает данных из Data Base
* Request Handler - API, к которому обращается Web-App, когда выполняет какой-либо запрос
* RAGH Module - получает текущий плейлист, возращает набор треков связанных с треками в текущем плейлисте и информацию о изначальном плейлисте
* AI Module - получает набор треков связанных с текущими и информацию о плейлисте, выбирает из них некоторое количество подходящих под определенные информацией плейлиста критерии, из них выбирает лучшие на основании того, как пользователи выбирали треки из рекомендаций до этого
* User Data Module - валидирует данные пользователя при регистрации и авторизации, проверяет наличие необходимых для выполнения действия разрешений у пользователя

### Расположение компонентов в системе
* Data Base, Request Handler, Data Uploader, AI Module, RAGH Module, User Data Module находятся в Azure.
* Web-App находится на устройстве пользователя
* Spotify API существует как 3-d party API

### Взаимодействие компонентов системы при запросах пользователя
#### Регистрация пользователя
* Подается запрос к Request Handeler
* Он перенаправляет запрос к User Data Module
* Проверяется корректность данных
* Data uploader создает новую строку в базе данных для пользователя с его данными
* User Data Module получает информацию об успешном выполнении запроса/ошибке.
* В Web-App возвращается подтверждение об успешной регистрации или ошибка о том, что данные аккаунта стримингового сервиса недействительны
#### Авторизация пользователя
* Подается запрос к Request Handler
* Запрос перенаправляется к User Data Module
* User Data Module подает запрос к Data Uploader
* Data Uploader ищет на сервере строку данного пользователя в базе данных и проверяется корректность пароля
* Если авторизация произошла успешна, то отправляется подтверждение и данные пользователя сохраняются в кэш Web-App
* Если авторизация не прошла успешна, то возвращается уведомление об ошибке
#### Поиск/проигрывание превью песни
* Подается запрос в Web-App
* Клиент обращается к интерфейсу для работы с API Spotify и импортирует данные о треках на сервер
* Данные о песне передаются от интерфейса в Web-App
* На приложение/сайте показывается трек/начинается воспроизведение его превью в зависимости от команды
#### Создание плейлиста
* Подается запрос к Request Handler
* Запрос перенаправляется к User Data Handler, он проверяет есть ли у пользователя возможность создать плейлист
* Data Uploader создает на сервере новый плейлист данного пользователя
* User Data Module получает информацию об успешном выполнении запроса/ошибке.
#### Обновление Плейлиста
* Подается запрос к Request Handler
* К RAGH Module подается запрос
* RAGH Module отправляет результат своей работы к AI Module
* AI Module выбирает из полученных данных подходящие под указанный контекст и наиболее часто выбираемые пользователями
* Информация передается Data Uploader, он загружает данные в Data Base
* Request Handler возвращает в Web-App обновленный плейлист
* Информация о плейлисте пользователя и сохраняется в кэш Web-App
* В Web-App отображается обновленный плейлист

