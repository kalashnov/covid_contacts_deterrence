# Оптимизация политики по ограничению COVID-19 контактов в Москве

Оперативный штаб Москвы, руководствуясь указом Мэра от 23 марта (№ 26-УМ), осуществляет меру по самоизоляции граждан в возрасте выше 65, обещая выплатить 2000 рублей пенсионерам, которые соблюдали карантин в период с 26 по 14 апреля. Такая постановка открывает возможность для оценки количества пенсионеров, на которых эта мера повлияла. Вкратце суть: если мы можем посчитать количество граждан в возрасте 65, которые были замечены на улице и лишины выплаты, а также лиц в возрасте 64 лет, которые были замечены на улице, на которых не распространяется мера, то разница между этими двумя числами дает хорошую оценку количества людей, которые остались дома именно из-за того, что им обещали выплату. Такой метод используют во всем мире для оценки государственной политики: например Angrist, J. D., & Lavy, V. (1999)

Вот так такой анализ может выглядеть (в рамках этой демонстрации использованы симулированные данные):

![Regression Discontinuity](/regression_discontinuity.png)

Если в дополнение к этому исследователь располагает демографической информацией, он может давать рекомендации по улучшению политики. Простой пример: предположим бюджет в среднем тратит на занятого в госсекторе пенсионера 500 рублей и снижает его вероятность появиться на улице на 10 процентных пунктов, а на занятого в частном секторе пенсионера 2000 рублей и снижает ее верояность появиться на улице на 20 процентных пунктов. В таком случае эффективно в выплатах приоретизировать госслужащих (10/500 > 20/2000). Конечно, чем больше демографической информации есть, тем лучше получается итоговая политика. Такой поход называется Policy learning и продвинутом варианте использует среди прочего методы машинного обучения (чаще всего леса с градиентным бустингом). Методы описаны в работах: Athey, S., & Wager, S. (2017), Zhou, Z., Athey, S., & Wager, S. (2018)

Вот примеры, как может выглядеть такой анализ (в рамках этой демонстрации использованы симулированные данные):

![Uplift](/uplift.png)

2000 рублей на человека никогда не тратится из-за нарушений карантина. По картинке видно, что осуществляя взвешенную политику можно без потери в эффекте сэкономить бюджет с 1600 рублей  в расчете на пенсионера до 1200. При бюджете в 800 рублей мы можем сохранить почти весь эффект и это лучше, чем наивное случайное правило в 2 раза. Также можно рассматривать эффектиные меры при низком бюджете, как в регионах (например 400 рублей в расчете на пенсионера)

Исследователь может соблюсти ограничения на социальную приемлемость политики, которая не должна дискриминировать по полу, поощрять скорее социально незащищенные слои населения. Методы по соблюдению таких ограничений описаны в работе Athey, S., & Wager, S. (2017). В результате получается интерпретируемое понятное правило вроде такого (взято из работы athey в контексте грантов на обучение)

Имея в руках данные мы можем подходить к таким вопросам: при ограниченном бюджете, кого эффективнее стимулировать денежно -- одиноких пенсионеров? незанятых пенсионеров? пенсионеров с инвалидностью?

# Литература

1. Athey, S., & Wager, S. (2017). Efficient policy learning. arXiv preprint arXiv:1702.02896.
2. Angrist, J. D., & Lavy, V. (1999). Using Maimonides' rule to estimate the effect of class size on scholastic achievement. The Quarterly journal of economics, 114(2), 533-575.
3. Zhou, Z., Athey, S., & Wager, S. (2018). Offline multi-action policy learning: Generalization and optimization. arXiv preprint arXiv:1810.04778.

 # Контакты
 
 Если вас заинтересовала эта симуляция, я буду рад пообщаться и ответить на вопросы по адресу go9513@gmail.com
