## Выбор локации для скважины
### Описание задачи
Допустим, мы работаем в добывающей компании «ГлавРосГосНефть». Нужно решить, где бурить новую скважину.

Нам предоставлены пробы нефти в трёх регионах: в каждом 10 000 месторождений, где измерили качество нефти и объём её запасов. Построим модель машинного обучения, которая поможет определить регион, где добыча принесёт наибольшую прибыль. Проанализируем возможную прибыль и риски техникой Bootstrap.

Шаги для выбора локации:

- В избранном регионе ищут месторождения, для каждого определяют значения признаков;
- Строят модель и оценивают объём запасов;
- Выбирают месторождения с самым высокими оценками значений. Количество месторождений зависит от бюджета компании и стоимости разработки одной скважины;
- Прибыль равна суммарной прибыли отобранных месторождений.

### Используемые инструменты
- Pandas
- NumPy
- Seaborn
- LinearRegression

### Результаты
В ходе данного исследования мы изучили данные по трем регионам и построили для каждой модель линейной регрессии.После этого рассчитали уже по этим данным среднюю прибыль и доверительный интервал. Нам нужно было, чтобы доля убытков была меньше 2,5%, что удалось обнаружить только для второго региона. Также у второго региона больше средняя прибыль по выборкам, а также метрика R2 для модели линейной регрессии почти близка к идеальной в отличии от моделей других регионов.