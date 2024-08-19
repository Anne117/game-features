# Выделение фич из описаний игр и генерация тэгов

Файл `suitable_tags.ipynb` представляет собой Jupyter Notebook, предназначенный для анализа описаний игр и выделения ключевых признаков (фич) для дальнейшего их использования. Принцип работы заключается в том, чтобы по входному эмбеддингу описания игры найти 10 похожих по описанию игр и выбрать из их тегов 20 наиболее встречающихся. Основные функции данного файла включают:

1. **Загрузка данных:**  
   Файл загружает данные об играх из CSV файла с помощью библиотеки pandas.

2. **Выделение фич из описаний:**  
   Используя предобученную модель Roberta, текст описаний игр преобразуется в эмбеддинги, которые затем используются для нахождения наиболее близких по смыслу описаний других игр.

3. **Генерация случайной игры:**  
   Код предусматривает генерацию случайной игры из датасета. После этого он автоматически составляет фичи для этой игры и сравнивает их с имеющимися в датасете.

4. **Подбор тэгов:**  
   На основе близости эмбеддингов с описаниями других игр подбираются 20 наиболее встречающихся тэгов, которые могут быть использованы для описания игры.

5. **Оценка полученных тэгов:**
   В коде предоставлена возможность перепроверить работу модели на играх и их тегах из датасета и увидеть результат в процентном соотношении. Данный способ оценивания является валидным, так как способ работы модели не предоставляет ей правильных ответов описание-тег в процессе обучения.

Этот файл полезен для тех, кто хочет автоматизировать процесс выделения ключевых признаков из описаний игр и генерации соответствующих тэгов, используя методы обработки естественного языка и машинного обучения.
