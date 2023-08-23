## Шифрование персональных данных клиентов
### Описание задачи
Нам нужно защитить данные клиентов страховой компании «Хоть потоп». Разработаем такой метод преобразования данных, чтобы по ним было сложно восстановить персональную информацию. Обоснуем корректность его работы.

Нужно защитить данные, чтобы при преобразовании качество моделей машинного обучения не ухудшилось. Подбирать наилучшую модель не требуется.

### Используемые инструменты
- Pandas
- Numpy
- LinearRegression


### Результаты
В ходе данного исследования мы проверяли возможность шифрования персональных данных клиентов, путем умножения матрицы признаков на квадратную обратимую матрицу. Таким образом мы можем получить другие данные, которые без декодирования постороннему человеку ничего не скажут. Мы математически обосновали, что умножение матрицы не окажет влияния на получаемые предсказания, а также придумали алгоритм сравнения моделей, где признаки кодировались и нет. В итоге мы реализовали алгоритм и практически подтвердили, что подобное кодирование не оказывает значимого влияния на качество моделей по метрике R2. 

Итого, данный метод можно применять для текущих моделей без потери качества.