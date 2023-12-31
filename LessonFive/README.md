# Урок 5. Другие виды тестирования
## Задание 1. 
*Представьте, что вы работаете над разработкой простого приложения для записной книжки, которое позволяет пользователям добавлять, редактировать и удалять контакты.
Ваша задача - придумать как можно больше различных тестов (юнит-тесты, интеграционные тесты, сквозные тесты) для этого приложения. Напишите название каждого теста, его тип и краткое описание того, что этот тест проверяет.

### Юнит тесты:
Для первоначальной проверки будут проводиться базовые тесты:
1) Добавление контакта;
2) Удаление контакта; 
3) Вывод контакта;
4) Редактирование контакта; 
5) Сохранение контакта;
6) Тест на правильность ввода(символы, буквы, цифры); 
Эти тесты основаны на быстрой проверке модулей кода. Данные тесты ориентированы на проверку правильности работы кода, используя при этом простые инструменты. 
Это своего рода детальное иследование. Проблемой данной тест процедуры в большой трудозатратности. Большое количество мелких тестов нужно будет часто исправлять и корректировать.
Также возникнут проблемы с графической составляющий.


### Интеграционные тесты:
Использование интеграционного тестирования связано с обменом данных в приложении. Само тестирование частично воссоздает реальную среду. Частый пример использования интеграционного тестирования это взаимосвязь с БД. Отсюда возникает сложность/минус работы с такими тестами -> увеличивается время тестирования. Так же можно считать связь с внешними компонентами тоже минусом, так как принимаемых данных может оказать большое количество. 
Будут использоваться следующие тесты: 
1) Обновление. Обновляет данные в нашей записной книге. Выкачивает информацию с бд;  
2) Проверка добавить существующий контакт. Система проверяет в бд на существование контакта; 
3) Получение списка контактов из бд;
  
### Сквозное тестирование:
Цель сквозного тестирование и анализ всего ПО. проверяются различные зависимости, связь с другими компанентами и целостность данных. В это тестирование входит интерфейс (фронт). Проводиться в самом конце. используется при этом реальные данные. Тесты проводят в специальной среде где имитируют рабочий процесс. 
1) Проверка на правильность заполнения формы при добавление контакта;
2) Правильность отображения вывода существующих контактов;
3) Процесс поиска и удаления контакта; 
4) Корректное отображение при редактировании. 

## Задание 2. 
*Ниже список тестовых сценариев. Ваша задача - определить тип каждого теста (юнит-тест, интеграционный тест, сквозной тест) и объяснить, почему вы так решили.

1) Проверка того, что функция addContact корректно добавляет новый контакт в список контактов.
-> Юнит-тест. 
Используется этот метод так как нужно в изолированной среде проверить работуспособность метода

2) Проверка того, что при добавлении контакта через пользовательский интерфейс, контакт корректно отображается в списке контактов.
-> Сквозное тестирование. 
Тестирование будет проводиться End-to-End. Т.е. начиная от пользовательского интерфейса заканчивая методом отображения контакта. При этом тестировании будут анализированиться корректность отображения для пользователя данные полученные из БД. 

3) Проверка полного цикла работы с контактом: создание контакта, его редактирование и последующее удаление. 
-> Интеграционное тестирование. 
В данном цикле происходит взаимосвязь с БД. Т.е. проверяются методы при котором данные сохраняются в бд. В последующем эти данные могут быть получены из БД для редактирования/удаления. 