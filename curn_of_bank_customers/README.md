## **Прогнозирование оттока клиента Банка**

**Описание:** 

* На основе данных из банка определить клиент, который может уйти.Из банка стали уходить клиенты. Каждый месяц. Немного, но заметно. Банковские маркетологи посчитали: сохранять текущих клиентов дешевле, чем привлекать новых.
Нужно спрогнозировать, уйдёт клиент из банка в ближайшее время или нет. Предоставлены исторические данные о поведении клиентов и расторжении договоров с банком.


**Инструменты:** 

* python, pandas, numpy,  sklearn, RandomForest


**Вывод:** 

Проведено прогнозирование оттока клиентов банка на основе исторических данных поведения клиентов: 
* Для прогнозирования было построено 12 моделей
* Отбор происходил по F1-мере, так же следили за acu-roc 
* Для баланса классов использовали три подхода upsampled, downsampled и взвешивание классов. В upsampled мы искусственно завышали выборку,в downsampled наоборот – выравнивая классы. 
* Лучшей моделью оказалась Случайный лес.
* Для проверки на тестовой выборке мы соединили обучающую и тестовую и переобучили нашу лучшую модель. Что дало F1=0.62 на тестовой выборке и auc-roc = 0.86.То есть заметно перешли порог, поставленный по бизнесом в 0,59
* Построил roc-кривую и убедился, что наша модель лучше случайной
* Задача выполнена 