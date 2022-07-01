Класс StartUI зависит от классов Input, Item, Tracker. Чтобы создать объект StartUI, нужно создать объекты Tracker, Input.

В крупных проектах могут быть классы, которые имеют много зависимостей.

Чтобы упростить создание такие объектов, программисты придумали концепцию "внедрение зависимостей" с английского DI - dependency injection.

Идея DI.

1. Есть хранилище объектов. В нем мы будем регистрировать классы, объекты которых хотим иметь в проекте.

В нашем примере мы зарегистрируем там Tracker, StartUI, ConsoleInput.

2. Хранилище в рамках DI называется Context, то есть объекты относящиеся к предметной области нашего проекта.

3. После регистрации классов Context начинает инициализацию объектов. Он стоит дерево зависимостей. Сначала он создает объекты без зависимостей.

А потом создаем объекты с зависимостями.

4. После инициализации программист может получить нужный объект из Context.

Давайте мы сделаем свою реализацию DI.

Для реализации DI используется два подхода: мета программирование, рефлексия.

В этом примере мы будем использовать рефлексию. Рефлексия позволяет узнать какие элементы имеет класс в процессе выполнения программы.

Обратите внимание, не нужно использовать код ранее написанных версий Tracker, используйте каркасы классов, описанных в этом задании.

0. Что такое DI? [#6876] 
1. 1. Spring DI. Запуск [#2091]
2. 3. @Autowired. Внедрение зависимости [#261276]