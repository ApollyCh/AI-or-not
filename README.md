<h1> AI or not </h1>

Для данного задания был выбран метод трансферного обучения, который включает использование предобученной модели. В качестве модели был выбран Vision Transformer (ViT). Трансформеры в основном применяются для обработки текста, однако методика, основанная на разбиении изображения на патчи и их последующей обработке с использованием трансформера, является эффективным решением для задачи классификации изображений.

Для данной задачи я выбрала предобученную модель ViT-B/16. Процесс файн-тюнинга включает следующие этапы:

1. Замораживание всех параметров модели, за исключением верхнего слоя классификации. Затем происходит изменение этого слоя на новый, который будет предсказывать 2 класса.
2. Обучение модели на датасете train.
3. Размораживание всех параметров модели и обучение модели с намного меньшим значением learning rate.


<img src="figs/vision-transformer-vit.png">
