# classifier_development
Разработка классификатора компаний на основе анализа ассоциированных открытых проектов

Основной проблемой, решаемой в данном исследовании, является определение характеристик (признаков), которые влияют на перспективность открытых проектов Github. Успех проекта – многогранное понятие, и без ясного понимания и точного определения решающий параметров невозможно эффективно анализировать существующие проекты и делать прогнозы об их успешности. 

Целью данной работы является разработка модели для классификации открытых проектов на Github, используя данные о репозиториях, полученные с помощью Github API. Для достижения этой цели будут решены следующие задачи: 
1. Сбор данных с платформы GitHub с помощью GitHub API;
2. Подготовка и очистка данных для дальнейшего анализа;
3. Проведение первичного статистического анализа для выявления зависимостей между признаками;
4. Создание классификатора, предсказывающий успех проектов на основе собранных данных;
5. Оценка качества работы классификатора;
6. Формирование выводов и дальнейших действий по улучшению модели.

Таким образом, данная работа направлена на разработку инструмента, который может быть использован разработчиками и организациями для прогнозирования успешности открытых проектов. Полученные результаты могут быть полезны для выявления трендов, поиска перспективных проектов для участия и инвестиций, а также для анализа эффективности существующих практик разработки. Разработанный классификатор может служить основой для создания рекомендательных систем, которые помогут участникам GitHub ориентироваться в мире открытого исходного кода.

Основные выводы:
1. Сложность задачи: классификация перспективных проектов требует более глубокого понимания факторов, влияющих на популярность;
2. Эффективность моделей: Ансамблевые методы показали лучшие результаты по сравнению с простыми алгоритмами, однако они нуждаются в расширении набора признаков;
3. Признаки, связанные с активностью проекта, важны, но не достаточны: такие признаки, как частота коммитов и количество дней с момента последнего обновления, показали определенную значимость, однако их влияние на популярность проекта оказалось недостаточным для уверенного разделения классов. Это говорит о том, что популярность репозиториев, скорее всего, определяется более сложными факторами, включая социальное взаимодействие и качество контента;
4. Роль языков программирования как признака: языки программирования оказались слабым предиктором популярности проектов;
5. Дисбаланс классов как ключевая проблема: значительный дисбаланс классов создал условия, при которых большинство моделей склонялись к игнорированию меньшинства (класс 1 – перспективные проекты);
6. Качество данных и его влияние на результат: высокий уровень шума и наличие аномалий в данных (например, устаревшие, но популярные проекты) усложнили обучение моделей и могли стать причиной низких метрик качества для класса перспективных проектов. Это подчёркивает необходимость предварительной очистки данных и анализа выбросов;
7. Лимиты интерпретируемости моделей: такие модели, как случайный лес и градиентный бустинг, обеспечили высокую точность для класса 0 (неперспективных проектов), но оставили пробелы в интерпретации того, почему определенные проекты классифицируются как перспективные. Это говорит о важности применения методов интерпретации, таких как SHAP или LIME, для углубления анализа.
8. Необходимость дополнительных признаков: существующий набор признаков оказался узким, и его расширение могло бы значительно улучшить результаты классификации. Например, полезными могли бы быть такие признаки, как количество участников в проекте, динамика роста звёзд, активность по созданию issues или pull requests и другие метрики, отражающие вовлеченность сообщества.

