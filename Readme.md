## DI

### Легенда

В рамках лекции мы посмотрели, как использовать Spring для связывания зависимостей.

Соответственно, возникает вопрос, почему бы его не использовать в вашем приложении с сервлетами и не заменить указанный
ниже код на DI со Spring:

```java
@Override
public void init(){
final var repository=new PostRepository();
final var service=new PostService(repository);
        controller=new PostController(service);
        }
```

### Задача

Замените код в методе `init` на DI со Spring с использованием следующих методов конфигурирования бинов:

1. Annotation Config (ветка `feature/di-annotation`)
1. Java Config (ветка `feature/di-java`)

Обратите внимание, что вся функциональность (CRUD), реализованная до этого, должна по-прежнему работать.