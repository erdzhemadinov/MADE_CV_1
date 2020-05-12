# MADE_CV_1
Первое задание по дисциплине CV академии MADE

Из того, что не зашло/особо помогло:
  - Аугментация (данных итак было достаточно для обучения)
  - Разделение датасета по размерам изображения и раздельное обучение. 
  - Добавление scheduler'a.
Архитектура: resnet34. resnet50 не влезал в память ноутбука. 

Идея: проблема заключалась в том, что часть изображений были большого размера и при попытке их сжать, падало качество предсказания, поскольку MSE очень чувствителен к большим ошибкам, которые возникали при попытке ресайзнуть изображение. Поэтому был увеличен размер масштабирования картинки и кропа и уменьшен размер батча. 

На Lb выдаёт модель выдаёт ~8.10432 (файл resnet50_submit_14.747937092883449.csv), что расходится с лидербордом, потому что в последний день, когда я учил нейросеть и доучил её/прервал на 20-й эпохе за 3 ч. до конца дедлайна, поставил формироваться сабмит около 21:00 по МСК, но не отправил его, поскольку уснул во время 20-ти минутного инференса, поскольку работал над кернелом в предыдущую ночь. Проснувшись в 00:12 МСК, 12 мая, отправил его как Late Submission. Такой Epic Fail и вообще победа по жизни. 

Поэтому финальная версия кернела может дать результат, отличный от того, что на лидерборде 8.52697 (10-е место).

