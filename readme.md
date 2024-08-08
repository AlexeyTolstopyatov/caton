# MOM - "My object model"
Язык для обозначения свойств объекта, который пришел во сне.

### Синтаксис
Опрелеления = теги из XML/XAML

### Типизация
 - ```()``` Множество - Список, который НЕ ДОЛЖЕН содержать похожие элементы
 - ```[]``` Список - Динамический массив данных. МОЖЕТ содержать одинаковые типы данных
 - ```""``` Строка - Сравнивается с типом ```String```
 - ```11``` Число - Сравнивается с типом ```Int32```
 - ```1.2``` Дробь - Сравнивается с ```Double``` 

Объект я видел не как список, а как множество определений
Множества = ```()```
```mom
car=(
  name="lexus"
  model="LX"
  engine="..."
  ?{ Закрытый комментарий }
)
```
Списки = ```[]```
```mom
library=(
  ?{Предположим, есть список книг на полке "Б"}
  shelf25=[
    "Бунин И.А. Собрание стихов ... 2008",
    "Биохимия. ... 2003"
  ]
)
```

# Вложения
Если уж дорастет до такого, то приложения можно хранить так же внутри описания

```mom
function=(
  name="absolute"
  returns="uint32"
  !{
    public static uint Absolute(){}
  }
)
```
