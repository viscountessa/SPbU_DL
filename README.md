# SPbU_DL
Deep Learning course

Домашнее задание 1:

Выбрать датасет с изображениями (можно MNIST)
	
Выбрать архитектуру нейронной сети, подходящую для вашей конфигурации (лучше всего обучать на GPU компьютера), объяснить выбор. Взять предобученные веса, например, для классификации по ImageNet и дообучить.
	
Реализовать:
	а) Обучение классификатора на основе выбранной архитектуры
	б) Итеративную аугментацию
	в) Итеративную разморозку слоёв
	г) Адаптивный learning rate
	
Сравнить результаты, например, для таких конфигураций:
	а) Чистый классификатор
	б) Классификатор + итеративная разморозка + адаптивный lr
	в) Классификатор + итеративная аугментация
	г) Классификатор + все методы улучшения
	
Сделать выводы.
Ссылка на выполненное задание: https://github.com/viscountessa/SPbU_DL/blob/hw1_intro_multimodal_classification/multimodal_classification%2Bpseudolabeling.ipynb

Домашнее задание 2:
	
Добавить в решение ДЗ 1 псевдолейблинг, сравнить результаты с лучшим из имеющихся классификаторов (можно сделать разделение train-test-val)
	
Придумать 3 отличающихся от рассказанных на занятии метрики качества поиска (во всем многообразии элементов поисковой выдачи) и объяснить, почему их можно брать в качестве основных для оценки качества. 
	
Придумать 3 отличающихся от рассказанных на занятии метода улучшения качества разметки релевантности и объяснить, как именно они улучшат качество.
	
Рассчитать p-value гипотезы "выдача google по запросу <выберите любой запрос> статистически значимо лучше, чем выдача yandex по этому же запросу". Оценку релевантности всех страниц выдачи, а также уровень значимости (порог, при котором мы отвергаем гипотезу) провести самостоятельно.


Домашнее задание 3, часть 1 (исправление теста):
	
Показать, какие из рассматриваемых метрик (precision, recall, f1, accuracy, roc-auc, pr-auc, specificity, ...) чувствительны к дисбалансу классов на примере бинарной классификации
	
Написать формулу F_beta и объяснить, на что влияет параметр beta, привести примеры, когда beta лучше брать отличным от 1
	
Привести пример расчета ROC-AUC на не менее, чем 6 предсказаниях
	
Провести micro-агрегацию precision и recall, сравнить с взвешенной (на примере)


Домашнее задание 3, часть 2 (по материалам занятия)
	
Применить не менее 5 рассказанных техник оптимизации вашей модели из ДЗ 1 и 2, описать результаты профилирования 
	
Конвертировать модель в OnnxRuntime или TensorRT (+2 доп балла за это) для инференса 
	
При помощи инференса вашей модели на ваших данных сгенерировать датасет из векторов (размер не менее 1000 векторов)
	
Реализовать product-квантизацию полученного датасета в экстремальном случае: M = D, то есть, каждая компонента вектора квантизуется независимо от других (соответственно, вместо кластеризации простой подбор порогов, при которых ошибка представления компоненты будет наименьшей)
