# Анализ результатов А/B-тестирования изменений после проведения акции в сети магазинов

## Описание проекта
В компании есть рекламная акция, в рамках которой клиенту дается возможность получить дополнительные баллы лояльности за покупку, совершенную в течение ограниченного периода времени после запуска акции.

Классическая акция подразумевает получение дополнительных 1000 баллов лояльности за покупку от 100 рублей. Было решено провести эксперимент, в рамках которого в тестовой группе предлагается в 2 раза больше баллов лояльности за покупку от 100 рублей. Эксперимент был проведен в шести торговых точках.

## Задачи проекта
- рассчитать результаты эксперимента (в целом и в отдельности по каждой точке)
- вынести решение об эффективности воздействия B по сравнению с воздействием A
- визуализировать результаты анализа

## Выводы
Для получения корректных результатов необходима правильная подготовка данных, поэтому в начале мы преобразовали данные:
- убрали пустые значения
- изменили тип данных столбца id_point на int
- удалили выбросы
- исключили из анализа точку продаж, в которой отсутствует контрольная группа.


Результаты AB тестирования по всем торговым точкам показывают, что начисление дополнительных 1000 баллов в рамках проведения акции, позволило увеличить средний чек.

В разрезе торговых точек видно, что в точках 1178 и 1179 разница в среднем чеке не имеет статистической значимости. В точке 1182 разница средних чеков составила примерно 910 рублей и она статистически значима. Таким образом весь наблюдаемый на общих по всем точкам данных эффект обусловлен одной этой точкой продаж. По точке 1199 отсутсвует контрольная группа. По точкам 1186 и 1188 недостаточно данных для анализа. Для того, чтобы сделать выводы, следует перезапустить тест.