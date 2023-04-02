
# MULTIMIGATOR

Проект в рамках курса по проектированию и производству электронных устройств на Физтех.Фабрике МФТИ

Результатом данной работы стала плата с поочередно мигающими диодами

![](modules/ROOT/images/migator.gif)  


---------------------------------------------------------------------------------------------------


Проектирование и изготовление состоит из следующих этапов:

### 1. Виртуальное моделирование

Делаем в Tinkercad и видим, что диоды горят (как и конденсаторы))

![example](modules/ROOT/images/plata0.png)  

### 2. Моделирование на макетной плате

Вручную собираем схему на учебной плате, чтобы проверить, как это будет работать

![example](modules/ROOT/images/plata-1.png)  

### 3. Разработка печатной платы

Проектирование платы производится в EasyEDA

Сначала собираем основную схему

![example](modules/ROOT/images/plata1.png)  

Затем преобразуем схему в следующий вид и располагаем их уже как на готовой плате

![example](modules/ROOT/images/plata2.png)  

### 4. Изготовление платы

Подготавливаем программу для фрезера в FlatCAM

На выходе получаем файл с кодом, указывающем станку каким образом мы хотим обработать плату: дорожки + дырки

![example](modules/ROOT/images/plata3.png)  

Загружаем программу в фрезер, устанавливаем нужный инструмент и запускаем станок

Результат раскроя

![example](modules/ROOT/images/plata4.png)  

### 5. Шелкография

Делаем с помощью лазера рисунок

![example](modules/ROOT/images/plata5.png)  

### 6. Пайка

Заключительным этапом припаиваем все элементы и приклеиваем батарейку

![](modules/ROOT/images/migator2.gif)  

Как и ожидалось, диоды мигают поочередно!

![example](modules/ROOT/images/plata6.png)  


### Интересный факт!

+ При прохождении максимального тока через диод, примыкающий к нему конденсатор полностью разряжен

+ При принебрежимо малом токе, когда диод почти не горит, конденсатор полностью заряжен в обратном направлении

В данной схеме использовались диоды, пропускающие ток в обоих направлениях, 

+ в одном - светятся зеленым
+ в другом - красным

Видно, что когда цепь размыкается в момент прохождения минимального тока через один из диодов (примыкающий к нему кондер заряжен в обратном направлении), то через этот диод полностью разряжается примыкающий кондер и мы видим красное свечение!

![](modules/ROOT/images/migator3.gif)  

