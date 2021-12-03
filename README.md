# Проекты по Аналитике данных
В этом репозитории размещены проекты, сделанные в процессе обучения на курсах Karpov.Courses "Аналитик данных", а так же тестовые задания.
Далее приведена общая информация о проекте и используемые инструменты в процессе выполнения проекта.

[id1]: https://github.com/cremona-olga/projects/tree/main/product_analytics_metrics
[id2]: https://github.com/cremona-olga/projects/tree/main/cars_analytics_regression
[id3]: https://github.com/cremona-olga/projects/tree/main/bootstrap
[id4]: https://github.com/cremona-olga/projects/tree/main/final_project_courses
[id5]: https://github.com/cremona-olga/projects/tree/main/netflix

| № | Проект | Описание | Инструменты |
| :- | :--------------------- | :---------------------------| :---------------------------|
| [1][id1]  | [Проект по продуктовой аналитике. Расчёт основных метрик продукта, когортный анализ, построение воронки][id1] |Рассчитан MAU, количество установок приложения по месяцам, произведён когортный анализ, построена воронка, найден наиболее эффективный канал привлечения пользователей. Выводы: Всего 12% пользователей совершило повторные покупки в течение первого квартала 2020г. MAU января превышает MAU февраля на 24%. Количество установок в феврале упало более, чем на 50% по сравнению с январём. Построив воронку мы отпределили, что самая низкая конверсия была из шага «Переход в корзину» в следующий шаг как для зарегестрированных, так и для незарегистрированных пользователей. Конверсия из установки в покупку была максимальной 01.01.2020. На графике когортного анализа, мы можем видеть, что конверсия в покупку больше всего у первой когорты на всех неделях. На второй неделе конверсия в два раза меньше (35%) для второй когорты, и начиная с третьей когорты больше 80% пользователей не совершает покупки уже на второй неделе. На последней неделе совершили покупки всего 1-4% пользователей и всех когорт, кроме первой. Больше всего новых пользователей перешло по рекламе в Яндексе, однако пользователи, пришедшие с Яндекса, имеют минимальную конверсию в первую покупку. Пользователи, пришедшие с реферальной программы, имеют медианный первый чек выше других. Самый высокий ROMI у канала ВК | Pandas, Numpy, Seaborn, Plotly, Seaborn, Matplotlib. Метрики продукта, предобработка данных, визуализация. |
| [2][id2]  | [Влияние характеристик автомобиля на стоимость][id2] | Имеются данные о стоимости автомобилей, необходимо понять, какие из характеристик влияют на стоимость. В работе было проанализировано, как характеристики машин влияют на их стоимость. Разобраны модели с разным количеством предикторов и оставлена модель с оптимальным их количеством. Выбранная модель объясняет примерно 90% дисперсии. Среди предикторов 10 из 27 оказались не значимыми (p > 0.05). Пример интерпретации: при единичном изменении показателя horsepower, цена возрастает на 86.8164. | Pandas, Matplotlib, Seaborn, Statsmodels. Линейная регрессия, предобработка данных, визуализация. |
| [3][id3]  | [Сравнение групп двумя способами: бутстрапом и u-тестом][id3] | Имеются данные со значениями метрики у групп "контроль" и "тест". Выводы: тестовая выборка имеет большие выбросы, что сильно искажает нам среднее значение; применяя бутстрап с оценкой среднего, мы могли бы отклонить нулевую гипотезу о равенстве средних и сделать вывод, что тестовая и контрольная выборка имеют различия; однако, тот же бутстрап, но уже по медиане не дает нам отклонить нулевую гипотезу, так как p-value сильно больше 0.05, т.к. здесь проверяется другая гипотеза; U-критерий Манна-Уитни так же не дал бы нам отклонить нулевую гипотезу. Оценки pvalue так же направлены как у бутстрапирования медианы. На основе непараметрического анализа, мы принимаем нулевую гипотезу о том, что распределения отличаются не значительно и не нужно внедрять изменения. |Statsmodels, Pandas, создание признаков, предобработка данных, визуализация. |
| [4][id4]  | [Итоговый проект на курсе Аналитик данных][id4] | Необходимо найти инсайты в данных продуктовых магазинов компании. 1. Мы выяснили, какие пары товаров пользователи чаще всего покупают вместе. Необходимо было найти паттерны покупок, что позволит оптимизировать размещение продуктов в магазине, для удобства пользователей и увеличения выручки. Выполнена предобработка данных, проведен первичный анализ данных, найдено 5 пар товаров чаще всего покупаемых вместе 2. Имеется информация о числе заказов за прошедшие 3 месяца с разрешением по неделям. Построить (если это возможно) прогноз продаж на следующие 3 месяца. Выполнена предобработка данных, проведен первичный анализ данных. Количества данных недостаточно для того, чтобы построить корректный прогноз. Желательно иметь данные более, чем за год для того, чтобы сделать прогноз с учетом сезонности. Построен прогноз продаж, хотя использовать его нежелательно. Посчитана линейная корреляция. Найдена формула регрессионной прямой. На основе построенной модели, рассчитан прогноз ещё на 14 недель вперёд. 3. Работа с базой данных. Составлен запрос в Clickhouse, с объединением данных из четырёх таблиц | Pandas, Seaborn, Matplotlib, Stats, Statsmodels, SQL |
| [5][id5]  | [Анализ фильмов производства Netflix][id5] | Были получены ответы на следующие вопросы: 1. Фильмы какого жанра наиболее популярные? А какого менее? 2. На каком языке Netflix чаще всего снимает фильмы? 3. Есть ли зависимость между длительностью фильма и его рейтингом? 4. Порекомендуйте, на какой месяц лучше всего запланировать премьеру нового фильма. Почему? | Pandas, Seaborn, Matplotlib, Stats, Statsmodels. Предобработка данных, визуализация, матрица корреляции, бутстрап, анализ данных. |


