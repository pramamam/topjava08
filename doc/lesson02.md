# Онлайн проекта <a href="https://github.com/JavaWebinar/topjava08">Topjava</a>

### <a href="https://drive.google.com/drive/folders/0B9Ye2auQ_NsFfkpsWE1uX19zV19IVHd0bTlDclc5QmhMMm4xa0Npek9DT18tdkwyLTBZdXM">Материалы занятия (скачать все патчи можно через Download папки patch)</a>

## ![hw](https://cloud.githubusercontent.com/assets/13649199/13672719/09593080-e6e7-11e5-81d1-5cb629c438ca.png) Разбор домашнего задания HW1:

### ![video](https://cloud.githubusercontent.com/assets/13649199/13672715/06dbc6ce-e6e7-11e5-81a9-04fbddb9e488.png) 1. <a href="https://drive.google.com/open?id=0B9Ye2auQ_NsFXzByNVF3VV9zM1k">отображения списка еды в JSP</a>
- **Apply 2-1-HW1.patch**
> Изменения в `MealsUtil`:
  - Сделал константу `List<Meal> MEALS`
  - Сделал вспомогательный метод `getWithExceeded`
> Форматирование даты сделал на основе <a href="http://stackoverflow.com/questions/35606551/jstl-localdatetime-format#35607225">JSTL LocalDateTime format</a>

- <a href="http://design-pattern.ru/patterns/mvc.html">MVC - Model View Controller</a>

### ![video](https://cloud.githubusercontent.com/assets/13649199/13672715/06dbc6ce-e6e7-11e5-81a9-04fbddb9e488.png) 2. <a href="https://drive.google.com/open?id=0B9Ye2auQ_NsFQndBeWFOa3phRTg">Optional: реализация CRUD</a>
- **Apply 2-2-HW1-optional.patch**

> Про repository будет подробно в видео "Слои приложения"

- <a href="http://stackoverflow.com/questions/246859/http-1-0-vs-1-1">HTTP 1.0 vs 1.1</a>

### ![question](https://cloud.githubusercontent.com/assets/13649199/13672858/9cd58692-e6e7-11e5-905d-c295d2a456f1.png) Вопросы по HW1

> Зачем в `InMemoryMealRepositoryImpl` наполнять map с помощью нестатического блока инициализации, а не в конструкторе?

Разницы нет. Сделал чтобы напомнить вам про эту конструкцию. См. <a href="https://habrahabr.ru/post/133237/">Малоизвестные особенности Java</a>

> Почему `InMemoryMealRepositoryImpl` не singleton?

По умолчанию бины Spring являются синглетонами (в его контексте). А все наши классы слоев приложения будут создаваться через Spring.

## Занятие 2:
### ![video](https://cloud.githubusercontent.com/assets/13649199/13672715/06dbc6ce-e6e7-11e5-81a9-04fbddb9e488.png) 3. <a href="https://drive.google.com/open?id=0B9Ye2auQ_NsFVDJZVTktQzRYTWc">Библиотека vs Фреймворк. Стандартные библиотеки Apache Commons, Guava</a>
-  <a href="http://commons.apache.org/">Apache Commons</a>, <a href="https://code.google.com/p/guava-libraries/wiki/GuavaExplained">Guava</a>

### ![video](https://cloud.githubusercontent.com/assets/13649199/13672715/06dbc6ce-e6e7-11e5-81a9-04fbddb9e488.png) 4. <a href="https://drive.google.com/open?id=0B9Ye2auQ_NsFeWZ1d1cxaUZiUmc">Слои приложения. Создание каркаса приложения.</a>
- **Apply 2-3-app-layers.patch**

>  Поменял `LoggedUser` на `AuthorizedUser`

> Про DTO еще можно будет посмотреть в видео Алименкова "Босиком по Граблям", когда мы добавим Hibernate

-  <a href="http://en.wikipedia.org/wiki/Multilayered_architecture">Паттерн "Слои приложения"</a>
-  <a href="https://www.genuitec.com/products/myeclipse/learning-center/spring/myeclipse-for-spring-reference-blueprints/">Архитектурные
            слои приложения в Spring</a>
-  <a href="https://ru.wikipedia.org/wiki/Data_Access_Object">Data Access Object</a>
-  <a href="http://codehelper.ru/questions/205/new/repository-и-dao-отличия-преимущества-недостатки">Паттерны Repository и DAO</a>
-  <a href="http://martinfowler.com/eaaCatalog/dataTransferObject.html">Паттерн DTO</a>
- <a href="http://stackoverflow.com/questions/1612334/difference-between-dto-vo-pojo-javabeans">Value Object и Data Transfer Object</a>
-  <a href="http://stackoverflow.com/questions/21554977/should-services-always-return-dtos-or-can-they-also-return-domain-models">Should services always return DTOs, or can they also return domain models?</a>

Справочник:
   - <a href="http://habrahabr.ru/post/263033/">Забудьте о DAO, используйте Repository</a>
   - <a href="http://stackoverflow.com/questions/6640784/difference-between-active-record-and-dao">Difference between Active Record and DAO</a>

###  ![video](https://cloud.githubusercontent.com/assets/13649199/13672715/06dbc6ce-e6e7-11e5-81a9-04fbddb9e488.png) 5. <a href="https://drive.google.com/open?id=0B9Ye2auQ_NsFWXA1b0pnMGlvU0U">Обзор  Spring Framework. Spring Context.</a>
- **Apply 2-4-add-spring-context.patch**
    -  <a href="http://en.wikipedia.org/wiki/Spring_Framework">Spring Framework</a>
    -  <a href="http://spring.io/projects">Проекты Spring</a>.
    -  <a href=http://docs.spring.io/spring/docs/current/spring-framework-reference/html/overview.html>Обзор Spring Framework</a>

- **Apply 2-5-add-dependency-injection.patch**
    -  <a href="https://ru.wikipedia.org/wiki/Инверсия_управления">Инверсия управления.</a>
    -  <a href="http://habrahabr.ru/post/131993/">IoC, DI, IoC-контейнер — Просто о простом</a>

- **Apply 2-6-add-annotation-processing.patch**
   -  <a href="http://stackoverflow.com/questions/6827752/whats-the-difference-between-component-repository-service-annotations-in">Difference
       between @Component, @Repository & @Service annotations in Spring</a>
   -  <a href="http://www.mkyong.com/spring/spring-auto-scanning-components/">Spring Auto Scanning Components</a>
   -  <a href="http://www.seostella.com/ru/article/2012/02/12/ispolzovanie-annotacii-autowired-v-spring-3.html">Использование аннотации @Autowired</a>

-  Справочник:
   -  <a href="http://image.slidesharecdn.com/springintroduction-130729220359-phpapp01/95/spring-introduction-3-638.jpg?cb=1375162442">DI/ Service Locator</a>
   -  <a href="http://docs.spring.io/spring/docs/current/spring-framework-reference/html/beans.html">Introduction to the Spring IoC container
       and beans</a>
   -  <a href="http://it.vaclav.kiev.ua/2010/12/25/spring-framework-for-begginers-part-7/">Constructor против Setter Injection </a>
   -  <a href="https://spring.io/guides">Getting Started</a>
   -  <a href="http://docs.spring.io/spring/docs/current/spring-framework-reference/htmlsingle/">Spring Framework Reference Documentation</a>
   -  <a href="https://github.com/spring-projects">Spring на GitHub</a>
   -  <a href="https://dzone.com/refcardz/spring-annotations">Spring Annotations</a>

### ![video](https://cloud.githubusercontent.com/assets/13649199/13672715/06dbc6ce-e6e7-11e5-81a9-04fbddb9e488.png) 6. <a href="https://drive.google.com/open?id=0B9Ye2auQ_NsFN2N6LS1PVE96SW8">Пояснения к HW2. Обработка Autowired</a>
  

## ![question](https://cloud.githubusercontent.com/assets/13649199/13672858/9cd58692-e6e7-11e5-905d-c295d2a456f1.png) Ваши вопросы
>  Какова цель деления приложения на слои?

Управляемость проекта (особенно большого) повышается на порядок:
- Обеспечивается меньшая связываемость. Допустим если мы меняем что то в контроллере, то сервис эти изменения не задевают.
- Облегчается тестирование (мы будем тестировать слои сервисов и контроллеров отдельно)

> DTO используются когда есть избыточность запросов, которую мы уменьшаем, собрав данные из разных бинов в один? Когда DTO необходимо использовать?

(D)TO может быть как частью одного entity  (набор полей) так и набором нескольких entities.
В нашем проекте для данных, которые надо отдавать наружу и они отличаются от Entiy (хранимый бин), мы будем делать (Data) Transfer Object и класть в отдельный пакет to.
Например `MealsWithExceeded` мы отдаем наружу и он является Transfer Object, его надо пернести в пакет `to`.
На многих проектах (и собеседованиях) практикуют разделение на уровне maven модулей entity слоя от логики и соответствующей конвертацией ВСЕХ Entity в TO, даже если у них те же самые поля.
Хороший ответ когда TO обязательны есть на <a href="http://stackoverflow.com/questions/21554977/should-services-always-return-dtos-or-can-they-also-return-domain-models#21569720">stackoverflow: When to Use</a>.

> Что такое схема в spring-app.xml xsi:schemaLocation и зачем она нужна

<a href="https://ru.wikipedia.org/wiki/XML_Schema">XML схема</a> нужна для валидации xml, IDEA делает по ней атвозаполнение.

> Почему контроллеры положили в папку web, а не в conrollers?

Тоже самое что `domain/model` - просто разные названия. `web` думаю даже чаще называют (например в <a href="https://github.com/spring-projects/spring-petclinic/tree/master/src/main/java/org/springframework/samples/petclinic">spring petclinic</a>)

> Что означает для Spring

     <bean class="ru.javawebinar.topjava.service.UserServiceImpl">
         <property name="repository" ref="mockUserRepository"/>
     </bean> ?

Можно сказать так: создай и занеси в свой контекст бин `UserServiceImpl` и заинжекть в его проперти из своего контекста бин `mockUserRepository`.

> Как биндинг происходит для `@Autowired`? Как поступать, если у нас больше одной реализации `UserRepository`?

`@Autowired`  инжектит по типу (т.е. ижектит класс который реализует `UserRepository`). Обычно он один. Если у нас несколько реализаций, Spring не поднимится и поругается - `No unique bean`.
 В этом случае <a href="http://www.mkyong.com/spring/spring-autowiring-qualifier-example/">можно уточнить имя бина через @Qualifier</a>. `@Qualifier` обычно добавляют только в случае нескольких реализаций.

> Зачем мы наследуем NotFoundException от RuntimeException?

Так с ним удобнее работать. И у нас нет никаких действий по восстановлению состояния приложения (no recoverable conditions): <a href="http://stackoverflow.com/questions/6115896/java-checked-vs-unchecked-exception-explanation">checked vs unchecked exception</a>. По последним данным checked exception вообще depricated: <a href="http://blog.takipi.com/ignore-checked-exceptions-all-the-cool-devs-are-doing-it-based-on-600000-java-projects">Ignore Checked Exceptions</a>

--------------------

## ![hw](https://cloud.githubusercontent.com/assets/13649199/13672719/09593080-e6e7-11e5-81d1-5cb629c438ca.png) Домашнее задание HW02

#### Реализовать `InMemoryUserRepository` и принадлежность еды конкретному пользователю:
- переименовать `MockUserRepositoryImpl` в `InMemoryUserRepositoryImpl` и имплементировать по аналогии с `InMemoryMealRepositoryImpl` (список пользователей возвращать отсортированным по имени)
- зарефакторить `MealRepository/InMemoryMealRepositoryImpl`:
  - еда принадлежит пользователю
  - список еды возвращать отсортированным по времени, последние записи наверху
  - если еда отсутствует или чужая, возвращать `null/false` (см. комментарии в `UserRepository`)
    
#### Реализовать слои приложения для функциональности "еда":
- Отнаследовать `Meal extends BaseEntity`, `MealWithExceed` переносим в пакет to (transfer objects)
- API контроллера должна удовлетворять все потребности демо приложения и ничего лишнего (см. <a href="http://topjava.herokuapp.com">демо</a>)
- после авторизации (сделаем позднее) запрос попадает в контроллер, методы которого будут доступны снаружи по http, т.е. в запрос можно будет сделать с ЛЮБЫМ id для еды 
  (не принадлежащем авторизированному пользователю, id авторизованного юзера будет попадать в `AuthorizedUser.id()`, см. реализацию `ProfileRestController`). Нельзя позволять модифицировать/смотреть чужую еду:
  - у еды есть УНИКАЛЬНОЕ id, по которому можно определить из базы, чья она;
  - если еда не принадлежит авторизированному пользователю или отсутствует, в `MealServiceImpl` бросать `NotFoundException`.
- Включить классы в контекст Spring и проверить из `SpringMain` вызов метода `MealRestController`
#### Примечания
- `AuthorizedUser` известен только на слое web (`MealService` можно тестировать без подмены логики авторизации), принимаем в методах сервиса и репозитория параметр `userId`: id владельца еды.
- Пока можно НЕ добавлять поля в `Meal` (добавим позже)
- В `MealServiceImpl` постараться сделать в каждом методе только одни запрос к `MealRepository`
- Еще раз: не надо в названиях методов повторять названия класса (`Meal`).

### Optional: связываем `MealServlet` с контекстом Spring. Позже, когда будем работать через Spring MVC, `MealServlet` удалим.

- В `MealServlet` сделать инициализацию Spring, достать `MealRestController` из контекста и работать с едой через него (см. `SpringMain`. `pom.xml` НЕ менять, работаем со `spring-context`).
- Добавить в `mealList.jsp` и `MealServlet` две отдельные фильтрации еды: по дате и по времени (см. демо)
- Добавить выбор текущего залогиненного пользователя (имитация авторизации, сделать Select с двумя элементами со значениями 1 и 2 в `index.html` и `AuthorizedUser.setId(userId)` в `UserServlet`).

---------------------
### ![error](https://cloud.githubusercontent.com/assets/13649199/13672935/ef09ec1e-e6e7-11e5-9f79-d1641c05cbe6.png) Подсказки по HW02 (для проверки, сначала сделайте самостоятельно!)

- `InMemoryUserRepositoryImpl.getByEmail` попробуйте сделать через stream
- `InMemoryUserRepositoryImpl.delete` попробуйте сделать за одно обращение к map
- `MealRestController` должен уметь обрабатывать запросы:
    - Отдать свою еду (для отображения в таблице, формат `List<MealWithExceed>`), запрос БЕЗ параметров
    - Отдать свою еду, отфильтрованную по startDate, startTime, endDate, endTime
    - Отдать/удалить свою еду по id, параметр запроса - id еды. 
                        Если еда с этим id чужая или отсутствует - `NotFoundException`
    - Сохранить/обновить еду, параметр запроса - Meal. Если обновляемая еда с этим id чужая или отсутствует - `NotFoundException`
- Т.к. контроллер позволяет управлять ТОЛЬКО своей едой, `userId` снаружи не приходит (см. `ProfileRestController`)
- Фильтрацию по датам правильнее опустить на уровень репозитория т.к. из базы будем брать сразу отфильтрованные по дням записи. Следите чтобы первый и последний день не были обрезаны, иначе сумма калорий будет неверная.
- Сервлет мы удалим, а контроллер останется, поэтому возвращать `List<MealWithExceed>` надо из контроллера.  Преобразование в `MealWithExceed`, если подходить строго, нужно делать в сервисе (to возвращается из сервиса). Но главное: код не должен дублировался. У нас преобразование происходит в util, поэтому я конверчу в контроллере (мне показалось так удобнее).
- Закрывать springContext в сервлете грамотнее всего в `HttpServlet.destroy()`: если где-то в контексте Spring будет ленивая инициализация, метод-фабрика, не синглетон-scope, то контекст понадобится при работе приложения. У нас такого нет, но делать надо все грамотно.
- Проверьте корректную обработку пустых значений date и time в контроллере
- Если запрашивается список и он пустой, всегда возвращайте `Collections.emptyList()`. По нему можно легко итерироваться без риска `NullPoinException`. В java 8 появились возможность вместо null использовать `Optional` (на самом деле давно уже была в библиотеках типа Guava), они полезны для цепочек вычислений. Я сторонник применять их, когда код становится проще и логичнее.
