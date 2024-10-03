# otpusk
![Static Badge](https://img.shields.io/badge/MAYAK_random)
![GitHub top language](https://img.shields.io/github/languages/top/seligor/MAYAK_random)
![GitHub issues](https://img.shields.io/github/issues/seligor/MAYAK_random)

## Установка
__скачать:__
```
git clone https://github.com/seligor/MAYAK_random.git
```
__создать виртуальное окружение:__
```
python3 -m venv venv
```
__активировать виртуальное окружение:__
```
source venv/bin/activate
```
__установить требуемые библиотеки в окружение:__
```
pip install -r requirements.txt
```
## Запуск
```python main.py```
Он автоматически создаст базу данных на основе таблицы и сделает резеарвные копии таблицы и базы данных

## Функционал:
![image](https://github.com/user-attachments/assets/d0de21c5-c0ae-47cb-9d31-2b6297eecb26)
В интерфейсе всего одна функциональная кнопка и выпадающий список месяцев. 
по умолчанию фокус устанавливается на текущий месяц и соответственно он и используется для проведения розыгрыша. 
При этом, если рассмотреть более подробно табличный файл, он содержит несколько листов, названных по наименованию месяца по русски. 

Если принудительно изменить месяц в выпадающем списке, программа будет работать в тем листом табличного файла, который соответствует названию выбранного месяца.
Это поведение распространяется как на обновление данных так и на очистку данных

![image](https://github.com/user-attachments/assets/fdc84f48-339e-4800-8403-d34ac1b172db)

При щелчке правой кнопкой мыши можно скопировать результаты розыгрыша в буфер обмена для дальнейшего использования (составления списка победителей, составление поста в соцсетях)
Так же присутствует возможность очистки списка победителей розыгрыша

![image](https://github.com/user-attachments/assets/e03096ab-d65b-4c40-bc51-932cee44aad7)

В верхнем меню "Файл" скрыта функция сброса результатов розыгрыша. 
Логика работы такова, что если был проведён некий тестовый розыгрыш, допустим за октябрь, то в табличном файл на листе "октябрь" будет заполнен столбец напротив победителей. 
При запуске функции сброса результатов розыгрыша этот столбец очищается. Так же очищается и список победителей в интерфейсе. То есть после выполнения этой функции можно приступать
к проведению розыгрыша "с чистого листа"


Что скрыто от глаз, но выполняется:
1. Создаются резервные копии базы данных и табличного файла при каждом запуске программы
2. Резервные копии старше 30 дней удаляются при запуске программы.


